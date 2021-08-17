# ZephyrNET - zephyr.network

![max and zfogg with zephyrnet](https://hackclub.slack.com/files/U01DV5F30CF/F02BUDA9VUH/img_5771.jpg?origin_team=T0266FRGM&origin_channel=D01EG2KRR6Y)

in this directory, you'll find the planning docs for the ZephyrNET. this includes a physical server, a hypervisor, virtual machines, docker containers, and all the code and config to make them work. the docs are unedited other than privacy redactions.

the idea of the hackathon was: because we're on a train, we won't have internet. so let's make our own `intranet`! and when we're done, we'll bring it back to HQ and put it online in read-only mode (or something). this will act as a sort of monument to the event.

There were two large components to the ZephyrNET: the core hardware, and the software platform that all 500 projects could be built and deployed on top of. You can find @zfogg's notes on hardware below, and @rishiosaur's notes on deployments in [zephyrnet.md](zephyrnet.md).

with love,
\- @zfogg, @rishiosaur, msw

## ZephyrNET Hardware

### Network

the network of ZephyrNET was simply a LAN. it was accessed via WiFi. i personally routed five train cars with ethernet and WiFi, along with my friend Dan Eckert who graciously donated his workweek time + networking equipment to Hack Club in order to make it all happen (thanks Dan!).

here's the gear we used:
* 1 Ubiquiti Unifi Dream Machine router
* 6 Ubiquiti Unifi AP-Lite wireless access points
* 1 Ubiquiti Unifi AP-LR (Long Range) wireless access point
* 400ft~ish of CAT5e / CAT7 ethernet cables (many of which were destroyed by traincar doors :rip:)

#### NYC -> Chicago

![zephyrnet on amtrak](https://hackclub.slack.com/files/U01DV5F30CF/F02B92NJ45U/img_20210718_163014514.jpg?origin_team=T0266FRGM&origin_channel=D01EG2KRR6Y)

we bought most of the seats in one Amtrak car. other passengers could still walk through. when we boarded, the conductor saw us bringing the zephyrnet server onboard and asked about power consumption. we basically were very friendly and got their permission to run ethernet down the luggage rack for wifi. it ended up going well, but many passengers who got on board were quite audibly confused. this stretch was for one night, and hack clubbers stayed in their seats in coach for the night.

![zephyrnet on amtrak again](https://hackclub.slack.com/files/U01DV5F30CF/F02BFQL0LMQ/img_20210718_163021214.jpg?origin_team=T0266FRGM&origin_channel=D01EG2KRR6Y)

#### Chicago -> San Francisco

three private train cars attached to an amtrak route. a "superdome" with a sleeper on either side. the server, router, and master switch on the bottom floor of the superdome with two access points on top. a leaf switch and two access points in each sleeper, with 100ft of ethernet running back to the master switch. the train doors scraped against the ethernet, exposing the shielding a few times (RIP purple cords).

![zephyrnet in chicago](https://hackclub.slack.com/files/U01DV5F30CF/F02BUDBNT7T/img_5653.jpg?origin_team=T0266FRGM&origin_channel=D01EG2KRR6Y)

#### San Francisco -> LA

the coastal starlight is the most beautiful route in the country. it was much like the first leg of the trip, except much prettier and not overnight. it went without a hitch and we had great intranet during this bit.

![zephyrnet in venice](https://hackclub.slack.com/files/U01DV5F30CF/F02B943SH5L/ezgif.com-gif-maker.gif?origin_team=T0266FRGM&origin_channel=D01EG2KRR6Y)

### Compute

the compute power provided to hackers was 1 `Dell Poweredge R720` server. the server ran `Proxmox Virtual Environment` as its base operating system, which is a "hypervisor" (the OS that runs your VMs) with a nice web interface for remote VM access and control. we made a community Ubuntu VM at `commie.zephyr.network` and every Zephyr passenger given an account with `sudoer as root` access ("it's probably fine.. what could go wrong!?"). anyone who wanted a virtual machine could ask me or use the proxmox webui themselves to spawn a virtual machine of their choice, and then remote-access it with their laptops. however, no one actually wanted to do this and people seemed to be having the most fun being on the same host as their other participants. i think that is really neat and could be a fun thing to do with clubs.

the server hardware included 192gb of ram, 32cores of cpu, 8 2tb hdds, and four gigabit ethernet ports, two power 750w supplies. our common virtual machine was issued about 128gb of ram and 16 cores, which leaves plenty of spare power for other virtual machines. the drives were put into RAID10 and given to the hypervisor which is running XFS filesytem.

### Case

the server case was custom-build out of wood. it was made with hinged doors on either end, latches for the doors, handles in verious spots for easy carrying, and wheels on the bottom. we made sure to get thick enough wheels for the weight of the server and the battery power supply, as well as making sure the wheels could support the weight. in hindsight, the wheels were too small and did not turn very well for the weight and shape of the box. after the trip we suspended the server in its box above our fridge in the HQ office kitchen, where it will host zephyrnet projects on the internet and live on forever.

### Afterlife

After some clean-up on the `commie` virtual machine that we all hosted projects on for the hackathon, we will take take that VM and turn it into a Proxmox "VM Template". Once per day, the VM will be killed and replaced by a new instance of `commie` from the VM Template. This essentially puts `commie` into a 24hour timeloop much like the movie "Groundhog Day".

The last thing I coded for this project is a few scripts to manage Wireguard VPN peer profiles for the `zephyrnet0` VPN that is setup on `commie` VM. Each participant has their own VPN profile and can use it to access ZephyrNET's custom DNS (*.zephyr domains) and even SSH into `commie` VM again. Remember!! Everything will get reset and all users will be logged out after the VM has been up for 24hours.

\- @zfogg
