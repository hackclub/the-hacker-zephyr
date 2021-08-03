# 🚂 The Hacker Zephyr 

[🗃 Planning Documents](#-planning-documents) | [💵 Finances](#-finances) | [💻 Associated Code Repositories](#-associated-code-repositories) | [☀️ Previous Work](#%EF%B8%8F-previous-work)

**In 2021, we chartered a train, [The Hacker Zephyr](https://zephyr.hackclub.com), across America, and hosted the world's longest hackathon onboard (3,502 miles on land).** This is the story of how we did it.

<img src="https://cloud-qefbe8o34-hack-club-bot.vercel.app/0image_from_ios__36_.jpg" width="600" />

_The Zephyr passing Rocky Flats, Colorado._

## Securing the Train

_TBC_

## The Launch & Applications

Launching the Hacker Zephyr began with this [cryptic video](https://twitter.com/hackclub/status/1396881237113966594) that we tweeted on the 24th of May. We'd follow this tweet up with a collection of more [cryptic tweets](assets/teasers.md), Tom Preston-Warner even created a [few of his own](assets/teasers.md#toms-hints)!

The goal of this cryptic tweeting was to build up excitement for a mysterious community meeting we'd be hosting on the Saturday the 29th of May. We announced this on Wednesday the 26th of May. Accompanying the announcement was a [ticketing system](https://github.com/hackclub/all-aboard-tickets), Hack Clubbers could react to the Slack announcement with the 🎟 emoji and would be sent their very own [digital ticket to the meeting](https://camo.githubusercontent.com/d5802c680357ab439dac7fd86a46089aee8cc007341c1c37ebe79ad8df3b54bc/68747470733a2f2f636c6f75642d3578686f30663736622d6861636b2d636c75622d626f742e76657263656c2e6170702f307469636b65742d31302e706e67). These were a massive hit, they're likely what caused this Slack announcement to get 400+ reaction which at the time of writing is a Hack Club record. 

Building excitement for the meeting was one thing, we also needed to pull off a great meeting that would convey how excited we all were. We planned to start with some [old videos of trains with "American" music](https://youtu.be/3pdemObt1kA), then transition to a short introduction statement which would be followed by our [main trailer video](https://www.youtube.com/watch?v=FfGRgc18mh0). Zach & Tom would both then both talk about the trip and it's goals, once they were finished we opened the floor for questions from hackers. You can watch the full call [here](https://www.youtube.com/watch?v=wQebTjTyF7M).

Now the secret was out we launched our [website](https://zephyr.hackclub.com) ([code](https://github.com/hackclub/all-aboard)) with all the information, a [parent's guide to the Zephyr](applications/parent_guide.pdf) and a [registration of interest form](applications/form.md). Being on a train, we were constrained by the [capacity of the train](assets/melody's_amazing_train_explainer/transcript.md) so we could only select a group of those who registered interest. During that process we would ourselves different questions each day such as: "Who are some awesome new club leaders who will get a ton out of this?" and "Who are some people who have been deep into Hack Club for a long time and will both get a lot out of this, but will also give a lot to other people on board?". 

Those invited were [called](applications/invite_call_script.md) to receive the news and would then receive an [email](applications/invite_email_template.md) and a more detailed [guide](applications/attendee_welcome_packet.pdf). This made the process feel really personal. They'd have seven days for both them and their parents to sign a [Memorandum of Understanding](applications/memorandum_of_understanding.pdf) to confirm their participation. 

Following this we'd invite them to a private channel, coordinate with them on travel arrangements, have them or their parents sign a [liability release](applications/liability_release.pdf) and for those under-18 have their parents sign the ["Freedom Waiver"](applications/freedom_waiver.pdf). After all this and packing, they were ready to enter the [Hackerland](notes/2021-06-29_hackerland.md) in Vermont.

## ZephyrNET & the Hackathon

Large parts of the train route across the country would be without wifi or cellular access. Amtrak provides wifi, but their wifi is generally not connected to the internet except while passing through towns. 

The solution we came up with was lugging a 116 lbs server around with us (60lbs server + 56lbs hand-made wood enclosure) along with networking equipment we could setup on Amtrak coaches as well as on our private cars. A full write-up on the hardware and software behind this is available in [`zephyrnet/`](./zephyrnet/).

We looked at our favorite hackathons (each wonderful in [their](https://ldjam.com/) [own](http://www.stupidhackathon.com/) [way](https://www.codeday.org/)) and tried to pull a bit from each when coming up with [the focus of the event](./notes/hackerland.md). The Zephyr would be an anti-hackathon. It'd take the experience back to the highs of the 2014 college hackathon experience.

The hackathon's theme was to build a time capsule– too many hackathons are forgotten the day after the event ends b/c their website goes down & their projects don't work (and usually didn't work by the end of it anyways). Everything on the ZephyrNET would be open-sourced, and everyone would contribute to a public scrapbook (forked from our [community scrapbook](https://scrapbook.hackclub.com) to work offline). The goal was to reach 500 contributions to the time capsule or else delete the folders of members that [volunteered](./zephyrnet/volunteers-to-deletion.md) (an opt-in version of the original idea to `rm -rf` the whole server).

## Building an Adventure of a Lifetime

_TBC_

## The Trip

_TBC_

<!-- 

This repo houses everything from the trip. Planning documents, financials, and GitHub repos.

We began at Hack Club HQ in Burlington, Vermont, travelled down south to New York City, west through Chicago, and crossed the Rockies on our way to San Francisco. From there, we followed the Pacific Ocean and finished at SpaceX in Los Angeles.

The challenge of the hackathon: if we can't have access to the internet, why not build our own?

We purchased and lugged a 116lb server with 192 GB of RAM across the country, and gave everyone onboard full root access to it. The goal was to make 500 contributions to the ZephyrNET before arriving in LA, or else some of the data would be deleted.

This repository contains the open sourced [planning documents](#-planning-documents), [finances](#-finances), and [code](#-associated-code-repositories) behind The Hacker Zephyr. If you find an issue with a document or would like to request more information about the trip, please file an issue [here](https://github.com/hackclub/the-hacker-zephyr/issues/new). -->

## 🗃 Planning Documents

Our planning docs are organized by topic into the following directories:

| File                      | Description                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------- |
| [./assets](/assets)       | Sketches, logos, videos, etc. that we used to market the Zephyr                                          |
| [./logistics](/logistics) | Documentation on planning, scheduling, coordinating, and other details                                   |
| [./notes](/notes)         | Assorted notes from staff                                                                                |
| [./slack](/slack)         | Announcements posted in Slack                                                                            |
| [./zephyrnet](/zephyrnet) | Technical documentation / notes on the hardware & software that went into building the Zephyr's intranet |

## 💵 Finances

The finances for the Hacker Zephyr have been open sourced [here](http://bank.hackclub.com/zephyr) through Hack Club Bank's [transparency mode](https://headwayapp.co/bank-changelog/transparent-finances-(optional-feature)-151427). We've also produced a transparency update which runs through all the finances, you can read here (coming soon).

## 💻 Associated Code Repositories

- [The Zephyr Chronicles (Offline Scrapbook Port)](https://github.com/hackclub/the-zephyr-chronicles)
- [All Aboard (zephyr.hackclub.com site)](https://github.com/hackclub/all-aboard)
- [Ticket issuing service for announcement](https://github.com/hackclub/all-aboard-tickets)
- [ZephyrNET Deployment Flow](https://github.com/hackclub/zephyr-deploy-service)
- [schedule.zephyr - event schedule](https://github.com/hackclub/zephyr-hub) (still private)
- [photowall.zephyr - example dynamic ZephyrNET app](https://github.com/hackclub/photowall.zephyr)
- [garden.zephyr - example static ZephyrNET app](https://github.com/hackclub/garden.zephyr)
- [start.zephyr - instructions for getting started on ZephyrNET](https://github.com/hackclub/start.zephyr) (ultimately not used)
- [captive portal for ZephyrNET](https://github.com/hackclub/captive.zephyr) (ultimately not used) 


## ☀️ Previous Work

We've previously run other summer projects:

| Year | Project                                                        | Description                                                                                                                                                                                                                                                                           |
| ---- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2021 | [The Hacker Zephyr](#-the-hacker-zephyr)                       | _This repo!_                                                                                                                                                                                                                                                                          |
| 2020 | [Summer of Making](https://summer.hackclub.com)                | $50k in hardware donations to teen hackers around the world + the creation of [Scrapbook](https://scrapbook.hackclub.com) ([code](https://github.com/hackclub/scrapbook))                                                                                                             |
| 2019 | [Flagship Summit](https://flagship.hackclub.com)               | IRL meetup of high school hackathon organizers and coding club leaders ([photos](https://photos.google.com/share/AF1QipO3hb2mN-Q16icE-M16d-06uHyXLmvd3Rw6b_f_oosfAX9SnOvnouPOyO79P7pR7Q?key=anphZTNFUERPWXV3YnJQV2VzVVVFMFFVcGRDc3hB))                                                |
| 2018 | [Hack Club Bank](https://hackclub.com/bank/)                   | We built and launched the first version of Hack Club Bank (read the [1st](https://medium.com/hackclub/hack-club-bank-a-bank-for-student-hackers-e5d894ea5375) and [2nd](https://medium.com/hackclub/hack-club-bank-is-now-live-for-everyone-including-you-884f7f54836f) announcement) |
| 2016 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2016) | Summer camp / further writing & testing workshops                                                                                                                                                                                                                                     |
| 2015 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2015) | Summer camp / testbed for Hack Club's first [workshops](https://workshops.hackclub.com) ([content](https://github.com/hackclub/hackclub/tree/main/workshops#readme))([code](https://github.com/hackclub/workshops))                                                                   |
