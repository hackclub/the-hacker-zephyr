# Deployments

The core idea behind Zephyr was to run a hackathon on a train. Hackathons exist almost purely as a way for like-minded builders to do what they do best: build. However, we quickly ran into an issue with the very notion of building on a train: there isn't any form of internet. Putting Starlink onto the train car itself would've been a non-starter, considering the fact that the clearance between the top of the train and the tunnels we'd be going through is far shorter than the satellite receiver.

All of this meant that hackers onboard the train would have to build the Internet by themselves—without NPM, PyPi, Vercel, Heroku, DigitalOcean, or anything else that developers usually take for granted. For the organizing team, however, it meant that we needed to provide an efficient way for students to deploy their ideas: building the Internet means actually, well, building it.

## Server

The server's components themselves can be found in 

## Ideas

We started off by evaluating what we wanted out of a deployment flow & out of the Internet itself. ZephyrNET's goal was to be as editable as possible—giving everyone sudo access meant that you'd be able to go anywhere on the Ubuntu VM (even other hackers' home directories!), or crash the server itself (thanks to @willdoescode for doing so in the first 3 hours).

Every project hosted on the ZephyrNET needed to be editable by everyone else; not just because it enables a greater degree of collaboration, but because it means that high-quality contributions are the *norm*. The deploy flow that we built needed to allow for centralized repositories—everything should be able to be hosted in a single place or symlinked to it.

## Implementation

## Problems