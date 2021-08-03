# Introduction

Below are excerpts from the private ZephyrNET planning repository created to work through deploy flows—initially, we created a captive-portal based authentication flow on an open network, then moved to a private-network based deploy flow.


These notes were done by @zrl, @zfogg, @rishiosaur and @msw.

# Hotspot popup

1. I connect to a network named "ZephyrNET" on my MacBook Air
2. There is a popup, like what I see on airport WiFi networks, that says "Welcome to the ZephyrNET" and has a directory of all the different things on the ZephyrNET (kind of like the Hidden Wiki)
3. I am able to access everything on the ZephyrNET without having to click "Approve" or "Accept" anywhere on the popup. It doesn't actually block access to the rest of the ZephyrNET, like other captive portals do.


#   Non-`git`  deploy flow for static sites

1.  I connect to a network named "ZephyrNET"
2.  I SSH into the ZephyrNET using my user account
3.  I notice a directory called  `zephyrnet`  in my home directory
4.  I  `cd`  into  `zephyrnet/`  and see a bunch of folders with names like  `deploy.zephyr`  and  `max-homepage.zephyr`
5.  I create a new folder called  `zrl.zephyr`
6.  I create a file called  `index.html`  in the new  `zrl.zephyr`  folder with the contents  `<h1>Hello!</h1>`
7.  In my web browser, I go to  [https://zrl.zephyr](https://zrl.zephyr/)  and see "Hello!" in heading text
8.  Over SSH, I run  `ls -al`  in the  `zrl.zephyr`  folder and see a folder called  `.git`, noticing that a git repo has been initialized
9.  I run  `git log`  and see a commit was automatically made from my user account with the commit message "Direct edits within /opt/zephyrnet"

# `git`  deploy flow for static sites

1.  I connect to a network named "ZephyrNET"
2.  On my local machine, I create a git repo and commit a static site with three files:  `index.html`,  `styles.css`, and  `main.js`
3.  I run  `git remote add origin zrl@mothership:treasure-hunt.zephyr`  inside the git repo, and then run  `git push --set-upstream origin master`. My push succeeds.
4.  In my web browser, I go to  [https://treasure-hunt.zephyr](https://treasure-hunt.zephyr/)  and see my  `index.html`  served
5.  I SSH into the ZephyrNET using my user account, run  `ls zephyrnet/`, and notice a directory called  `treasure-hunt.zephyr`  has been created
6.  I run  `ls zephyrnet/treasure-hunt.zephyr/`  and see three files printed:  `index.html`,  `styles.css`, and  `main.js`
