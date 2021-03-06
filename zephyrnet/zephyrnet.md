# Deployments

The core idea behind Zephyr was to run a hackathon on a train. Hackathons exist almost purely as a way for like-minded makers to do what they do best: build. However, we quickly ran into an issue with the very notion of building on a train: there isn't any form of internet. Putting Starlink onto the train car itself would've been a non-starter, considering the fact that the clearance between the top of the train and the tunnels we'd be going through is far shorter than the satellite receiver.

All of this meant that hackers onboard the train would have to build the Internet by themselves—without NPM, PyPi, Vercel, Heroku, DigitalOcean, or anything else that developers usually take for granted. For the organizing team, however, it meant that we needed to provide an efficient way for students to deploy their ideas: building the Internet means actually, well, building it.


## Ideas

We started off by evaluating what we wanted out of a deployment flow & out of the Internet itself. ZephyrNET's goal was to be as editable as possible—giving everyone sudo access meant that you'd be able to go anywhere on the Ubuntu VM (even other hackers' home directories!), or crash the server itself (special thanks to @willdoescode for doing so in the first 3 hours).

Every project hosted on the ZephyrNET needed to be editable by everyone else; not just because it enables a greater degree of collaboration, but because it means that high-quality contributions are the *norm*. The deploy flow that we built needed to allow for centralized repositories—everything should be able to be hosted in a single place or symlinked to it. Every deploy needed had a `.zephyr` domain on the train, for easy access

We settled on a directory-based deployment setup, where creating a folder in `/opt/zephyrnet` was all that you needed to get started programming. You can find the full flows that were sketched out in [deployments.md](deployments.md). In essence, deployments were split up into two different types: static and dynamic deployments.

Static deployments linked a `.zephyr` domain to static files—create `x.zephyr` in `/opt/zephyrnet`, drop an `index.html` into it, and `x.zephyr` is instantly live, zero configuration needed.

Dynamic deployments linked some form of server that exposes a port (like an Express server) to a `.zephyr` domain. Create a `.zephyr` folder in the Zephyrnet directory, create an `entrypoint.sh` file (which holds a script for setup; think `npm start` and so forth) and/or `build.sh` (holds a script for building the server; consider `next build`), and run `git add . && git commit -m '<message>' && git push deploy master` to deploy a repository to be instantly live on ZephyrNET.

## Implementation

The deploy flow itself *seemed* fairly sound in theory (we'll get to some of the issues a bit later), and built upon already-proven techniques for deployment. Implementing it was another struggle, though—building great developer tools is an art, and two weeks to build a scalable PaaS (platform-as-a-service) is a time crunch in and of itself.

We started off by creating a [small script](https://github.com/hackclub/zephyr-deploy-service/blob/master/create.bash) using `inotifywait` to watch for new folder creations in `/opt/zephyrnet` (you can use `-e` to filter through events), which ran [a Node script](https://github.com/hackclub/zephyr-deploy-service/blob/master/deploy.js) to [set up Git](https://github.com/hackclub/zephyr-deploy-service/blob/bcf8349308f7c3eb4f01d4e52e747a1408261152/deploy.js#L31) and added [a simple README](https://github.com/hackclub/zephyr-deploy-service/blob/master/README_template.hbs) to the repository. Every dynamic repository had Git set up in it, for easier deployments from anywhere.

There were two key files that we were watching for (because we needed to see the first level of the source directories, we had to do a recursive search): `entrypoint.sh` and `index.html`. If an `index.html` file was created, the only thing that had to be done was create [an NGINX configuration file](https://github.com/hackclub/zephyr-deploy-service/blob/master/static_conf_template.hbs) with a simple `try_files` clause in a virtual host for the given domain.

If an `entrypoint.sh` file was created and pushed to the `deploy` remote (because all Git repositories are stateless and act as their own servers, hackers could push to a separate repository in `/opt/zephyr/watcher/repos`—you can still find the runtime files there!), a port would be allocated through [`ports.js`](https://github.com/hackclub/zephyr-deploy-service/blob/master/ports.js) (which writes a domain to a randomly named file in `/opt/zephyr/watcher/ports`) and [an NGINX configuration](https://github.com/hackclub/zephyr-deploy-service/blob/master/dynamic_conf_template.hbs) with a `proxy_pass` to the port running locally. To run the server, a [`systemd` configuration](https://github.com/hackclub/zephyr-deploy-service/blob/master/systemd-unit-template.service.hbs) is also generated, with a `bash /path/to/entrypoint.sh` located within. Instead of trying to do manual port allocations, we supplied a [PORT variable](https://github.com/hackclub/zephyr-deploy-service/blob/bcf8349308f7c3eb4f01d4e52e747a1408261152/systemd-unit-template.service.hbs#L13) in the environment (for something like Node, this could be accessed using `process.env.PORT`).

All deployments were done on the `git` user for isolation, and all `systemctl` services needed to be run after `su`ing or `ssh`ing into it.

The Commie VM (the virtual machine where all operations took place) had an instance of PowerDNS running on port 9191, which is what we used (along with dns_masq) to create custom TLDs. You can see the wrapper we used at [`pdns.js`](https://github.com/hackclub/zephyr-deploy-service/blob/master/pdns.js).

## Problems

- weird assumptions– thought people would SSH, but many didn’t know how
-  people started setting up rsync configs & would overwrite their .git folders, breaking our carefully orchestrated deploy flow
- people didn't know to check the auto-generated README, or wouldn't read through the steps
- the provided git steps were broken– the switch from master to main wasn’t consistent for everyone & it broke stuff when people couldn’t push/pull to the primary branch
- inotifywait would clog up when people did big filesystem operations (some people were scripting file creation & it would back up—there was a mutex lock on our ports directory, which slowed everything down and prevented parallelization)
- if someone created an index.html, then created an entrypoint.sh, we didn’t handle that edgecase—instead of updating the config files to use `proxy_pass`, the deploy flow kept the `try_files` clause, leading to 502 errors everywhere.
