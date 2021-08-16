# 🚂 The Hacker Zephyr 

[💻 Website](https://zephyr.hackclub.com) | [🗃 Planning Documents](#-planning-documents) | [💵 Finances](#-finances) | [💻 Associated Code Repositories](#-associated-code-repositories) | [☀️ In Years Past](#%EF%B8%8F-in-years-past)

Every summer, Hack Clubbers do something special.

In 2019, 75 Hack Club leaders gathered in San Francisco for [Flagship](https://photos.google.com/share/AF1QipO3hb2mN-Q16icE-M16d-06uHyXLmvd3Rw6b_f_oosfAX9SnOvnouPOyO79P7pR7Q?key=anphZTNFUERPWXV3YnJQV2VzVVVFMFFVcGRDc3hB). 

In 2020, 300 Hack Clubbers received $50,000 for hardware projects. We launched [Scrapbook](https://scrapbook.hackclub.com/), and hosted the [Summer of Making](https://summer.hackclub.com/).

**In 2021, we chartered a train, [The Hacker Zephyr](https://zephyr.hackclub.com), across America, and hosted the world's longest hackathon onboard (3,502 miles on land).**

This is the story of how we did it.

[<img src="https://cloud-ha70ck9ah-hack-club-bot.vercel.app/0the_hacker_zephyr_compressed.gif" width="100%" />](https://youtu.be/7pvGNYPR9KQ)  
_The Zephyr passing through Rocky Flats, Colorado with 42 Hack Clubbers on board._  

Hack Club is a transparent and open source 501(c)(3) nonprofit. In this repo, we'll break down each step of the planning behind The Hacker Zephyr, including coming up with the original idea, securing the train, how we thought about structuring the hackathon itself, the ZephyrNET and how it worked (and a read-only copy of it on the internet), and the finances - including a  transparent ledger of every single dollar spent.

We believe that coding is a sacred act, and spaces like hackathons can help bring coding to more people in an inspired, creative way. That's what they did for everyone on the Hack Club HQ team. Our hope is that the future of hackathons can be more creative, more hacker-focused, and more about building cool things with your friends, and that's what we tried to create on the Zephyr.

## Securing the Train

It turns out chartering a train across America is actually quite a difficult thing to do. The heyday of America's rail network in 1940s was quite expansive, but today more than half the routes are closed and there's only one company still operating passenger service: Amtrak.

<img src="https://cloud-3jwomswh7-hack-club-bot.vercel.app/05969009.jpg" width="39%" alt="Image of 1940s rail map in the USA" /> <img src="https://cloud-e5wyo56ga-hack-club-bot.vercel.app/0gv4sw.png" width="56%" alt="Image of Amtrak rail map" />  
_America's passenger rail network in the 1940s vs. today._

We spent the first three weeks of planning purely focused on one question: is it even possible, logistically, to get 42 Hack Clubbers on a train across the country (and at the tailend of a pandemic, at that)?

After looking at Amtrak availability, talking with others who have done similar trips, and spending hours on the phone with train enthusiasts, we were able to narrow down the possibilities to three options:

1. Book everyone purely in Amtrak cars
2. Source private cars from around the country and do a private charter
3. Do some sort of combination of the two

The benefit of Amtrak was the price, and perhaps the easiest to buy tickets for, but the downsides would be that attendees would have to wear masks, wouldn't have their own space, we'd share the space with other Amtrak passengers, and there could be many transfers. Additionally, all food would need to be prepackaged & we couldn't serve our own meals.

The benefit of the full charter was that we'd have our own space we could control, could serve meals onboard, not have masks, get a bed for everybody, and other things that made a private charter about 1000x better. The downside was that private charters are much more expensive & harder to find. In the past 2-3 years, a [recent policy change](https://www.bloomberg.com/news/articles/2019-03-25/can-you-buy-your-own-train-here-s-what-it-takes) made it even harder for private charters to operate. Many of the private charter owners we talked to went out of business over the past year or so because of the change.

We decided to go with the best of both worlds: a combination of the two. We'd take a bus from Burlington, Vermont to New York City, then Amtrak to Chicago, and then we'd board 3 private cars for the longest segment of the trip: from Chicago to Denver then San Francisco (55 hours). This private car ended up being the Superdome, the last of an initial 8 remaining in the US. Finally, we'd take Amtrak for the final and shortest leg of the trip, from SF to LA, where we'd end at SpaceX and Venice Beach.

After 40+ meetings with different groups in the train industry, train enthusiasts, and with Amtrak (including a failed attempt to meet with Amtrak's CEO), we finally found AAPRCO, the American Association of Private Railroad Car Owners, and specifically Steve Sandberg. It turns out that over the past 50 years as railroads have gone out of business and sold off their assets, normal individuals would go to the liquidation office and buy full railcars from the 40s and 50s at incredibly low prices. Steve is the largest private railcar owner in the country that we know of & he owns 14 cars and 2 locomotives. His cars were used in the George Bush Sr. 1992 presidential campaign train.

We met with Steve, and while he was originally aprehensive because he'd need to source a car from another part of the country to meet our needs, he agreed to do it and make The Hacker Zephyr happen.

In the end we had 3 train cars, 2 pullman sleepers, and the [Superdome](https://en.wikipedia.org/wiki/Super_Dome_(railcar)). Steve was onboard the whole way with his crew helping make the trip special.

We worked with Steve to bring as many Hack Clubbers along with us, but we ran into a [physical constraint at Denver Station](./assets/melody's_amazing_train_explainer/README.md). Even with the 3 cars the train was so long we [blocked](https://cloud-4cijeqoyj-hack-club-bot.vercel.app/0screen_shot_2021-08-05_at_10.44.51.png) [traffic](https://cloud-4cijeqoyj-hack-club-bot.vercel.app/1db526030-0219-483e-b1f4-513583e3c70b_1_105_c.jpeg) at any of the stops we made.

## The Launch & Applications

Launching The Hacker Zephyr began with this [cryptic video](https://twitter.com/hackclub/status/1396881237113966594) that we tweeted on the 24th of May. We'd follow this tweet up with a collection of more [cryptic tweets](assets/teasers.md), Tom Preston-Warner even created a [few of his own](assets/teasers.md#toms-hints)!

The goal of this cryptic tweeting was to build up excitement for a mysterious community meeting we'd be hosting on the Saturday the 29th of May. We announced this on Wednesday the 26th of May. Accompanying the announcement was a [ticketing system](https://github.com/hackclub/all-aboard-tickets), Hack Clubbers could react to the Slack announcement with the 🎟 emoji and would be sent their very own [digital ticket to the meeting](https://camo.githubusercontent.com/d5802c680357ab439dac7fd86a46089aee8cc007341c1c37ebe79ad8df3b54bc/68747470733a2f2f636c6f75642d3578686f30663736622d6861636b2d636c75622d626f742e76657263656c2e6170702f307469636b65742d31302e706e67). These were a massive hit, they're likely what caused this Slack announcement to get 400+ reactions which at the time of writing is a Hack Club record.

<img src="https://tickets.hackclub.com/api/ticket?username=USNPNJXNX" width="600" alt="Example of a ticket" />

Building excitement for the meeting was one thing, we also needed to pull off a great meeting that would convey how excited we all were. We planned to start with some [old videos of trains with "American" music](https://youtu.be/3pdemObt1kA), then transition to a short introduction statement which would be followed by our [main trailer video](https://www.youtube.com/watch?v=FfGRgc18mh0). Zach & Tom would both then both talk about the trip and it's goals, once they were finished we opened the floor for questions from hackers. You can watch the full call [here](https://www.youtube.com/watch?v=wQebTjTyF7M).

Now the secret was out we launched our [website](https://zephyr.hackclub.com) ([code](https://github.com/hackclub/all-aboard)) with all the information, a [parent's guide to the Zephyr](applications/parent_guide.pdf) and a [registration of interest form](applications/form.md). Being on a train, we were constrained by the [capacity of the train](assets/melody's_amazing_train_explainer/transcript.md) so we could only select a group of those who registered interest. During that process we would ourselves different questions each day such as: "Who are some awesome new club leaders who will get a ton out of this?" and "Who are some people who have been deep into Hack Club for a long time and will both get a lot out of this, but will also give a lot to other people on board?". 

Those invited were [called](applications/invite_call_script.md) to receive the news and would then receive an [email](applications/invite_email_template.md) and a more detailed [guide](applications/attendee_welcome_packet.pdf). This made the process feel really personal. They'd have seven days for both them and their parents to sign a [Memorandum of Understanding](applications/memorandum_of_understanding.pdf) to confirm their participation. 

Following this we'd invite them to a private channel, coordinate with them on travel arrangements, have them or their parents sign a [liability release](applications/liability_release.pdf) and for those under-18 have their parents sign the ["Freedom Waiver"](applications/freedom_waiver.pdf). After all this and packing, they were ready to enter the [Hackerland](./notes/2021-06-30_hackerland.md) in Vermont.

## ZephyrNET & the Hackathon

Large parts of the train route across the country would be without wifi or cellular access. Amtrak provides wifi, but their wifi is generally not connected to the internet except when passing through towns.

<img src="https://cloud-djzf1kkgk-hack-club-bot.vercel.app/0image_from_ios.jpg" width="350" alt="On the train with the ZephyrNet" />

The solution we came up with was lugging a 116 lbs server around with us (60lbs server + 56lbs hand-made wood enclosure) along with networking equipment we could setup on Amtrak coaches as well as on our private cars, called the ZephyrNET. A full write-up on the hardware and software behind this is available in [`zephyrnet/`](./zephyrnet/).

We looked at our favorite hackathons (each wonderful in [their](https://ldjam.com/) [own](http://www.stupidhackathon.com/) [way](https://www.codeday.org/)) and tried to pull a bit from each when coming up with [the focus of the event](./notes/2021-06-30_hackerland.md). The Zephyr would be an anti-hackathon. It'd take the experience back to the highs of the 2014 college hackathon experience.

The hackathon's theme was to build a time capsule. Too many hackathons are forgotten the day after the event ends b/c their website goes down & their projects don't work (and usually didn't work by the end of it anyways). Everything on the ZephyrNET would be open-sourced, and everyone would contribute to a public scrapbook (forked from our [community scrapbook](https://scrapbook.hackclub.com) to work offline), and there would be no prizes or judging. The goal was to reach 500 contributions to the time capsule or else delete the folders of members that [volunteered](./zephyrnet/volunteers-to-deletion.md) (an opt-in version of the original idea to `rm -rf` the whole server).

## The Trip

Coding is one of the most surreal activities a human can do. In a matter of hours you can take something from not existing to existing. Once you do that you can start to understand how the whole internet to the universe at large can exist. Hack Club believes that coding is a creative activity. To do inspired, creative work you need to have inspired experiences and be in an inspiring settings. With that, we wanted The Hacker Zephyr to be unlike any other hackathon. There would be no API prizes, no sponsor talks, and no sponsor talks at opening ceremony.

Instead, we wanted The Hacker Zephyr to feel like something could happen at any moment. We wanted it to be a place outside of the 'default world', particularly for high schoolers who are stuck with classrooms and college admissions always at the back (or forefront) of their minds.

So, we called up every weirdo, creative, and out of this box thinker we knew. Our first call was to [Woody Keppel](https://woodykeppel.com/), an incredible actor and performer, and professional clown. Woody brought in Jeremy Holm ([IMDB](https://www.imdb.com/name/nm3124435/)), who would later storm down the isles of an Amtrak coach in an ape suit with Woody in hot pursuit, as a zookeeper, among other things.

<img src="https://cloud-9dyk4ybpe-hack-club-bot.vercel.app/0screenshot_2021-08-05_at_1.09.15_pm.png" width="450" alt="An Ape on Amtrak!" />

Woody was the mastermind behind making the experience what it was and he made it feel like a _wholesome_ David Lynch movie. For example, on our first night, he hid a marching band in the trees that stormed in serendipitously, which was quite the surprise. As the sun set into the Rockies, Woody transformed the SuperDome into the "Hacker Lounge", with a full non-alcoholic cocktail menu and black tie service. He brought a band onboard, including one member called "Saw" who - between acts playing the violin - played a literal handsaw using his violin's bow. On our last night, Woody tended to a bonfire on the beach in Los Angeles and sung the song he composed about The Hacker Zephyr with everyone, called [42 Riders](https://42.zephyrnet.hackclub.com/).

Over the course of the journey we were visited by [Jerry](https://en.wikipedia.org/wiki/Jerry_Greenfield) from [Ben & Jerry's](https://www.benjerry.com/), [the Libermans](https://instagram.com/libermans/) (political exiles from Russia and previous Heads of Product at Snapchat), [Tom Preston-Werner](https://tom.preston-werner.com/) (GitHub, SemVer, Toml, RedwoodJS), [Zeb Scoville](https://twitter.com/explorer_flight) ([NASA flight director](https://www.nytimes.com/2021/08/02/science/nasa-space-station-zebulon-scoville.html)), and Cliff Stoll ([mad scientist](https://www.wired.com/story/meet-the-mad-scientist-who-wrote-the-book-on-how-to-hunt-hackers/)).

With all of this, and Woody + Jeremy's magic, passing through the Rocky Mountains at 10k ft. with the band playing, it was a surreal hackathon experience we don't think anyone will experience again. We hope that in the future it will inspire hackathons with a similar spirit.

<img src="https://cloud-k18c7grqc-hack-club-bot.vercel.app/0spacex_and_hack_club.jpg" width="600" alt="Hack Club at SpaceX" />

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

The finances for the Hacker Zephyr will be open sourced [here](http://bank.hackclub.com/zephyr) through Hack Club Bank's [transparency mode](https://headwayapp.co/bank-changelog/transparent-finances-(optional-feature)-151427) once we've filtered out all the personal info.

## 💻 Associated Code Repositories

- [The Zephyr Chronicles (Offline Scrapbook Port)](https://github.com/hackclub/the-zephyr-chronicles)
- [All Aboard (zephyr.hackclub.com site)](https://github.com/hackclub/all-aboard)
- [Ticket issuing service for announcement](https://github.com/hackclub/all-aboard-tickets)
- [ZephyrNET Deployment Flow](https://github.com/hackclub/zephyr-deploy-service)
- [schedule.zephyr - event schedule](https://github.com/hackclub/zephyr-hub)
- [photowall.zephyr - example dynamic ZephyrNET app](https://github.com/hackclub/photowall.zephyr)
- [garden.zephyr - example static ZephyrNET app](https://github.com/hackclub/garden.zephyr)
- [start.zephyr - instructions for getting started on ZephyrNET](https://github.com/hackclub/start.zephyr/tree/master/start.zephyr)
- [captive portal for ZephyrNET](https://github.com/hackclub/captive.zephyr) (ultimately not used) 

## ☀️ In Years Past

We've previously ran other summer projects:

| Year | Project                                                        | Description                                                                                                                                                                                                                                                                           |
| ---- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2021 | [The Hacker Zephyr](#-the-hacker-zephyr)                       | _This repo!_                                                                                                                                                                                                                                                                          |
| 2020 | [Summer of Making](https://summer.hackclub.com)                | $50k in hardware donations to teen hackers around the world + the creation of [Scrapbook](https://scrapbook.hackclub.com) ([code](https://github.com/hackclub/scrapbook))                                                                                                             |
| 2019 | [Flagship Summit](https://flagship.hackclub.com)               | IRL meetup of high school hackathon organizers and coding club leaders ([photos](https://photos.google.com/share/AF1QipO3hb2mN-Q16icE-M16d-06uHyXLmvd3Rw6b_f_oosfAX9SnOvnouPOyO79P7pR7Q?key=anphZTNFUERPWXV3YnJQV2VzVVVFMFFVcGRDc3hB))                                                |
| 2018 | [Hack Club Bank](https://hackclub.com/bank/)                   | We built and launched the first version of Hack Club Bank (read the [1st](https://medium.com/hackclub/hack-club-bank-a-bank-for-student-hackers-e5d894ea5375) and [2nd](https://medium.com/hackclub/hack-club-bank-is-now-live-for-everyone-including-you-884f7f54836f) announcement) |
| 2016 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2016) | Summer camp / further writing & testing workshops                                                                                                                                                                                                                                     |
| 2015 | [Hack Camp](https://github.com/hackclub/camp/tree/master/2015) | Summer camp / testbed for Hack Club's first [workshops](https://workshops.hackclub.com) ([content](https://github.com/hackclub/hackclub/tree/main/workshops#readme))([code](https://github.com/hackclub/workshops))                                                                   |
