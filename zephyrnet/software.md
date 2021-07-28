ZephyrNET

# ://zephyr.net software

People can edit, please reload

- An open server? Shared hosting!

- selective sudo (actually do sudo requests)
  - Allow all apt commands instantly, review all others
  - Also have a way to add a command to the sudo &quot;whitelist&quot; (like devzat needs sudo)
- Custom screen-fetch

## Hard Requirements

- ~~Compute~~
  - ~~VMs? Maybe a hypervisor?~~

- ~~proxmox, zenserver, or another~~
- ~~Libvirt is another idea too (make your choice of linux distro)~~

  - ~~Shared hosting?~~
    - ~~Pros: absolute chaos~~

- ~~Network~~
  - ~~DNS \*.zephyr \*.z~~
  - Dhcp
  - Dnsmasq
  - Pfsense

- Storage
  - raid0(?) 4x 1tb hdd
  - Fileserver with jellyfin?

- Telemetry
  - ELK - ElasticSearch, Logstash, Kibana
  - Prometheus(?)
  - Custom dashboard that logs and charts traffic between all our devices
    - Auth via slack then use your sshkey to sign a message

## Extra Services

- Mail
  - [https://wiki.archlinux.org/title/Sendmail](https://wiki.archlinux.org/title/Sendmail)
- Chat
  - Irc? Probably
  - Devzat! [quackduck/devzat: The devs are over here at devzat, chat over SSH!](https://github.com/quackduck/devzat)
  - Mattermost? Prolly not
  - [BeeBEEP - Free Office Messenger - Official Website](https://www.beebeep.net/)
  - bertie!!
  - xmpp?
  - Matrix!! - Definitely matrix because there are mobile phone clients, web clients, TONS of clients, it&#39;s realtime, and it&#39;s persistent (Ian / Yoda)
  - teamspeak? ventrilo? mumble?
  - jitsi!!

- Minecraft server
  -
- Software dev services
  - [Gitea.io](http://gitea.io/)
  - [ExtraHop System User Guide](https://docs.extrahop.com/current/eh-system-user-guide/)
  - GHE
- Databases
  - Postgres (managed)
  - Maria (managed)
  - Mongo (on-demand)
  - Redis (on-demand)
  - Elasticsearch (on-demand)
- Internet Docs and Resources
  - Adafruit + Sparkfun Hardware
  - [Practical Electronics for Inventors Book](http://instrumentacion.qi.fcen.uba.ar/libro/Scherz.pdf)
  - Tensorflow
  - Numpy
  - Pandas
  - ~~Kiwix (project gutenberg…)~~
    - [Kiwix Library](https://docs.google.com/spreadsheets/d/1lWXdwy3OIfZ1Ob2cQR707OMHSva3khTcAXZE9MK9ad8/edit#gid=598202886)
    - [~~Kiwix Library~~](https://docs.google.com/spreadsheets/d/1lWXdwy3OIfZ1Ob2cQR707OMHSva3khTcAXZE9MK9ad8/edit#gid=598202886)
  - Wiki
  - Wikipedia
  - Stackexchange (various)
  - README
  - [Crates.io](https://crates.io/) - Rust packages (anirudh will probably be setting up a mirror, the code for this doesn&#39;t exist yet so early access to the server will be helpful for dev)
  - ~~Npm registry powered by verdaccio (rishi)~~
  - Harbor for docker images (matt gleich)
  - Caprover (matt gleich)
  - Minecraft server (very important someone should do this)
- Packages
  - Maybe a place to list packages for each language on ZephyrNET? (aiden)
    - Possibly write down packages in this doc (categorized by lang)
- Fileserver
  - train movies from max
  - Normal movies from disney+ netflix hulu and prime video from sarthak