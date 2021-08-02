# 🚂 The Hacker Zephyr 

[🗃 Planning Documents](#-planning-documents) | [💵 Finances](#-finances) | [💻 Associated Code Repositories](#-associated-code-repositories) | [☀️ Previous Work](#%EF%B8%8F-previous-work)

**In 2021, we chartered a train, [The Hacker Zephyr](https://zephyr.hackclub.com), across America, and hosted the world's longest hackathon onboard (3,502 miles on land).** This is the story of how we did it.

<img src="https://cloud-qefbe8o34-hack-club-bot.vercel.app/0image_from_ios__36_.jpg" width="600" />

_The Zephyr passing Rocky Flats, Colorado._

### The Idea

_TBC_

### Securing the Train

_TBC_

### The Launch & Applications

Launching the Hacker Zephyr began with this [cryptic video](https://twitter.com/hackclub/status/1396881237113966594) created using [MapSCII](https://github.com/rastapasta/mapscii) & [cool-retro-term](https://github.com/Swordfish90/cool-retro-term) that we tweeted on the 24th of May. We'd follow this tweet up with a collection of more [cryptic tweets](assets/teasers.md), Tom Preston-Warner even created a [few of his own](assets/teasers.md#toms)!

The goal of this cryptic tweeting was to build up excitement for a mysterious community meeting we'd be hosting on the Saturday the 29th of May. We announced this on Wednesday the 26th of May. Accompanying the announcement was a ticketing system, Hack Clubbers could react to the Slack announcement with the :admission_tickets: emoji and would be sent there very own digital ticket to the meeting. These were a massive hit, they're likely what caused this Slack announcement to get 400+ reaction which at the time of writing is a Hack Club record. This system was built using Next.js & it's API routes, to generate each image we used headless Chromium to render an HTML page and take a screenshot of the result which then would be cached. 

Building excitement for the meeting was one thing, we also needed to pull off a great meeting that would convey how excited we all were. 

### ZephyrNET & the Hackathon

_TBC_

### Building an Adventure of a Lifetime

_TBC_

### The Trip

_TBC_

<!-- 

This repo houses everything from the trip. Planning documents, financials, and GitHub repos.

<<<<<<< HEAD
We began at Hack Club HQ in Burlington, Vermont, travelled down south to New York City, west through Chicago, and crossed the Rockies on our way to San Francisco. From there, we followed the Pacific Ocean and finished at SpaceX in Los Angeles.

The challenge of the hackathon: if we can't have access to the internet, why not build our own?

We purchased and lugged a 116lb server with 192 GB of RAM across the country, and gave everyone onboard full root access to it. The goal was to make 500 contributions to the ZephyrNET before arriving in LA, or else some of the data would be deleted.

This repository contains the open sourced [planning documents](#-planning-documents), [finances](#-finances), and [code](#-associated-code-repositories) behind The Hacker Zephyr. If you find an issue with a document or would like to request more information about the trip, please file an issue [here](https://github.com/hackclub/the-hacker-zephyr/issues/new). -->



=======
>>>>>>> 51f9352 (Remove narrative section from README)
## 🗃 Planning Documents

Our planning docs are organized by topic into the following directories:

| File                                                                                          | Description                                                                    |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [/assets](/assets)                                                    | Sketches, logos, videos, etc. that we used to market the Zephyr |
| [/logistics](/logistics) | Documentation on planning, scheduling, coordinating, and other details |
| [/notes](/notes)                                                                            | Assorted notes from staff |
| [/zephyrnet](/zephyrnet)                                                                    | Technical documentation / notes on the hardware & software that went into building the Zephyr's intranet |

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

| Year | Project                                                        | Description                                                                                                                                                                                                                            |
| ---- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2021 | [The Hacker Zephyr](#-the-hacker-zephyr)                       | _This repo!_                                                                                                                                                                                                                           |
| 2020 | [Summer of Making](https://summer.hackclub.com)                | $50k in hardware donations to teen hackers around the world + the creation of [Scrapbook](https://scrapbook.hackclub.com) ([code](https://github.com/hackclub/scrapbook))                                                              |
| 2019 | [Flagship Summit](https://flagship.hackclub.com)               | IRL meetup of high school hackathon organizers and coding club leaders ([photos](https://photos.google.com/share/AF1QipO3hb2mN-Q16icE-M16d-06uHyXLmvd3Rw6b_f_oosfAX9SnOvnouPOyO79P7pR7Q?key=anphZTNFUERPWXV3YnJQV2VzVVVFMFFVcGRDc3hB)) |
| 2018 | [Hack Club Bank](https://hackclub.com/bank/)                   | We built and launched the first version of Hack Club Bank (read the [1st](https://medium.com/hackclub/hack-club-bank-a-bank-for-student-hackers-e5d894ea5375) and [2nd](https://medium.com/hackclub/hack-club-bank-is-now-live-for-everyone-including-you-884f7f54836f) announcement) |
| 2016 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2016) | Summer camp / further writing & testing workshops                                                                                                                                                                                      |
| 2015 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2015) | Summer camp / testbed for Hack Club's first [workshops](https://workshops.hackclub.com) ([content](https://github.com/hackclub/hackclub/tree/main/workshops#readme))([code](https://github.com/hackclub/workshops))                    |
