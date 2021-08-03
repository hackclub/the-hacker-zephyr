# 🚂 The Hacker Zephyr 

[🗃 Planning Documents](#-planning-documents) | [💵 Finances](#-finances) | [💻 Associated Code Repositories](#-associated-code-repositories) | [☀️ Previous Work](#%EF%B8%8F-previous-work)

**In 2021, we chartered a train, [The Hacker Zephyr](https://zephyr.hackclub.com), across America, and hosted the world's longest hackathon onboard (3,502 miles on land).** This is the story of how we did it.

[<img src="https://cloud-qefbe8o34-hack-club-bot.vercel.app/0image_from_ios__36_.jpg" width="600" />](https://youtu.be/7pvGNYPR9KQ)

_The Zephyr passing Rocky Flats, Colorado with 42 Hack Clubbers on board._

## Securing the Train

Charting a train across america is actually quite a hard thing to do. They heyday of america's railnetwork in 1940s was quite expansive (image). Today more than half the routes are clsesd and there is only one company in charge (amtrak w/ route image)

When we looked at our options for securing a train that could support 50 hackers across the country, we had 3 options:

1. purely amtrak
2. find a nation-wide charter that would take us from burlington to la
3. combination of the two

The pros of amtrak were that id' be cheapest, and perhaps the easiest tto buy tickets for, but the downsides were that we'd have to wear masks, wouldn' t havae our own space, share the space with other amtrak passengers & cwould have many transfers. Amtrak cons is that all food would need to be prepackaged & we couldn't serve meals

The benefit of the full charger is that we'd have our own space we can control, we can serve meals onboard, we can set covid policy (no masks), we could get a bed for everybody, and other thnings that made a private charter about 1000x better. the downside is that private chargers are much more expensive & harder to find. In the past 2-3 year (link to rule change) a recent policy chaange makde it even harder for private charters to operate. Many of the private charter owners we talked to went out of business over the past year or so beecause of the cahnge.

We decided to go with the best of both worlds: a combination of the two. We'd take amtrak from burlington vermont to new york city, then chicago, and then we'd board 3 private cars for the longest segment of the trip: from chicago to denver then san francisco (55 hours). Finally we'd take amtrak for the final and shortest leg of the trip, from SF to LA, where we'd end at SpaceX

After 40+ meetings with different groups in the train industry, trayin enthusiists, and with amtrak (including a failed attempt to meet with Amtrak's CEO), we finally found AAPRCO, the american association...., and specifically steve samburg (spelling). It turns out that over the past 50 years as railroads have gone out of business and sold off their assets, normal indiviauls (hobyists) would go to the liquidation office and buy full railcars from the 40s and 50s at incredibly low prices. Steve is the largest private railcar owner in the country that we know of & he owns 18 cars (check this number) and 2 locomotives. He was also hired by the Clinton + Al Gore campaign in 1996 (which they won) and used the same car we used (check this).

We met with steve, and while he was originally aprehensive b/c he'd need to source a car from another part of the country to meet our needs, he agreed to do it and make the hacker zephyr happen.

In the end we had 3 train cars, 2 pullman sleepers, and the SUPERDOME (link & images). Steve was onbord the whole way with his crew helping make the trip special.

We worked with Steve to bring as many hack clubbers along with us, but we ran into a physi8cal constraint in denver station. Even with the 3 cars the tarin was so long we blocked traffic at any of the stops we made (ian photo).

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

<!-- ## Building an Adventure of a Lifetime

_TBC_ -->

## The Trip



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
