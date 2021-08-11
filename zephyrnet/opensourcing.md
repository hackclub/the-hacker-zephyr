# Open Sourcing Strategies

Of course, building the projects was only half the battle. For the ZephyrNET to work as a time capsule, everything built on top of it needed to be publicly accessible.

## Stage 1: Systemd

Obviously, the first step towards open sourcing projects has to do with getting the projects running. The ZephyrNET deploy flow used a thin wrapper on top of `systemd`, which encapsulated the start procedures for all the server-based projects (static projects are always loaded up—NGINX just serves static files), so to start up all the projects, one may loop over all the files in `/Users/git/.config/systemd/user` and run `systemctl start`:

```bash
#!/usr/bin/env sh

set -x
for filename in ~/.config/systemd/user/zephyrnet-*.zephyr-deployment.service; do
	systemctl --user enable "$(basename $filename)"
	systemctl --user start "$(basename $filename)"
done
set +x
```

This was the temporary solution we built on the train, to quickly restart every project all at once. Of course, any good server needs to be resilient—in the event of server crashes, one cannot rely on humans to fix them. That's why we moved the targets for every systemd configuration to start when the system reaches run level 2 (when a non-graphics shell for multiple users is spun up, using the `multi-user.target` target). With this addition, we didn't have to worry about keeping the services alive manually; whenever resets happened, they would just automatically boot up.
## Stage 2: DNS, NGINX & SSL

After getting the services working locally, the next step was making the bridge from private runs to public ones.

When connected to the ZephyrNET (through VPN or LAN), a `.zephyr` TLD is available, which is the primary form of interaction for the projects build on the train. Of course, `.zephyr` does not exist in real life, so we had to make all the projects work with a `.zephyrnet.hackclub.com` TLD: instead of going to `zoogle.zephyr`, for instance, you might go to `zoogle.zephyrnet.hackclub.com`.

In order to hook the ZephyrNET up to the rest of the internet, we first had to configure DNS for it. We used a revolving DNS service to point to our local IP for DNS resolution: [hackclub.myftp.biz](https://github.com/hackclub/dns/blob/c949cd2b14846099ab12aea32734edb458cf079e/hackclub.com.yaml#L50) points directly to the moving IP of ZephyrNET running through Comcast's network. We started off by creating wildcard domains in PowerDNS (the DNS management service running onboard the server)—that routed the `*.zephyrnet.hackclub.com` domain to our internal domain before moving on to scripting the creation of individual domains, generated from the contents of `/opt/zephyrnet`.

After getting DNS working, we had to generate SSL certificates for all the websites—on the public internet, the trust-levels are very different. Onboard the train, we were dealing with a medium-to-high trust environment, and built our systems to be quite open. On the public internet, though, a level of trust needs to be estabished to have a great user experience (on both ends). We began by registering the `.zephyrnet.hackclub.com` ending as a zone on LetsEncrypt (Certbot has great compatibility with NGINX), which allowed us to link to the same certificates from all the NGINX configs:
```

server {

listen 443 ssl;
        server_name community.zephyrnet.hackclub.com www.community.zephyrnet.hackclub.com;

        ssl_certificate /etc/letsencrypt/live/zephyrnet.hackclub.com/fullchain.pem; # managed by Certbot
        ssl_certificate_key /etc/letsencrypt/live/zephyrnet.hackclub.com/privkey.pem; # managed by Certbot
        root /opt/zephyrnet/community.zephyr;
        index index.html index.htm index.nginx-debian.html;

		location / {
			sub_filter '.zephyr' '.zephyrnet.hackclub.com';
			sub_filter_once off;
              proxy_pass http://127.0.0.1:33951/; 
        }

}

server {
    if ($host = community.zephyrnet.hackclub.com) {
        return 301 https://$host$request_uri;
    } # managed by Certbot

 root /opt/zephyrnet/community.zephyr;
        index index.html index.htm index.nginx-debian.html;

        listen 80;
        server_name community.zephyr www.community.zephyr;
	server_name community.zephyrnet.hackclub.com www.community.zephyrnet.hackclub.com;
location / {
sub_filter '.zephyr' '.zephyrnet.hackclub.com';
sub_filter_once off;
               proxy_pass http://127.0.0.1:33951/; 
        }

location = /robots.txt {
  add_header  Content-Type  text/plain;
  return 200 "User-agent: *
Disallow: /";
}

}
```

We also disabled search engine indexing for every project except chronicles, to prevent inadvertent private data collection.