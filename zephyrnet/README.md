# ZephyrNET - zephyr.network

in this directory, you'll find the planning docs for the ZephyrNET. this includes a physical server, a hypervisor, virtual machines, docker containers, and all the code and config to make them work. the docs are unedited other than privacy redactions.

the idea of the hackathon was: because we're on a train, we won't have internet. so let's make our own `intranet`! and when we're done, we'll bring it back to HQ and put it online in read-only mode (or something). this will act as a sort of monument to the event.

There were two large components to the ZephyrNET: the core hardware, and the software platform that all 500 projects could be built and deployed on top of. You can find @zfogg's notes on hardware below, and @rishiosaur's notes on deployments in [zephyrnet.md](zephyrnet.md).

{{{ FIXME: add more good vibez etc here. i'm not crying you're crying }}}

with love,  
\- @zfogg, @rishiosaur, msw


## ZephyrNET Hardware

### Network

the network of ZephyrNET was simply a LAN. it was accessed via WiFi. i personally routed five train cars with ethernet and WiFi, along with my friend Dan Eckert who graciously donated his workweek time + networking equiptment to Hack Club in order to make it all happen (thanks Dan!).

the gear we used is:
* 1 Ubiquiti Unifi Dream Machine router
* 6 Ubiquiti Unifi AP-Lite wireless access points
* 1 Ubiquiti Unifi AP-LR (Long Range) wireless access point
* 400ft~ish of CAT5e / CAT7 ethernet cables (many of which were destroyed by traincar doors :rip:)

#### NYC -> Chicago

we bought most of the seats in one Amtrak car. other passengers could still walk through. when we boarded, the conducter saw us bringing zephyrnet server onboard and asked about power consumption. we basically were very friendly and got their permission to run ethernet down the luggage rack for wifi. it ended up going well, but many passengers who got on board were quite audibly confused. this stretch was for one night, and hack clubbers stayed in their seats in coach for the night.

#### Chicago -> San Francisco

three private train cars attached to an amtrak route. a "superdome" with a sleeper on either side. the server, router, and master switch on the bottom floor of the superdome with two access points on top. a leaf switch and two access points in each sleeper, with 100ft of ethernet running back to the master switch. the train doors scraped against the ethernet, exposing the shielding a few times (RIP purple cords).

#### San Francisco -> LA

the coastal starlight is the most beaufitul route in the country. it was much like the first leg of the trip, except much prettier and not overnight. it went without a hitch and we had great intranet during this bit.

### Compute

the compute power provided to hackers was 1 `Dell Poweredge R720` server. the server ran `Proxmox Virtual Environment` as its base operating system, which is a "hypervisor" (the OS that runs your VMs) with a nice web interface for remote VM access and control. we made a community Ubuntu VM at `commie.zephyr.network` and every Zephyr passenger given an account with `sudoer as root` access ("it's probably fine.. what could go wrong!?"). anyone who wanted a virtual machine could ask me or use the proxmox webui themselves to spawn a virtual machine of their choice, and then remote-access it with their laptops. however, no one actually wanted to do this and people seemed to be having the most fun being on the same host as their other participants. i think that is really neat and could be a fun thing to do with clubs.
