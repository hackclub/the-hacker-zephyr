# To Do

To-do for wrap-up more generally:

- [ ] Final email sent out to all on board

- [ ] Everyone on team gets all their reimbursements in

  - [x] Zach Latta
  - [x] Max
  - [ ] Zach Fogg
  - [ ] Christina
  - [ ] Tina
  - [ ] Woody
  - [ ] Matthew

- [ ] Anything Hack Club needs to get reimbursed for from teammates (ex. ticket costs)

- [ ] Pay all contractors / actors, including any bonuses

- [ ] Thank you notes

- [ ] Lost playing cards, lost Diamond Age books

- [ ] Get a bunch of money from American Airlines for messing up so many flights and stranding Hack Clubbers

  - At least $196 x 2 for hotels for Lux and Rebecca when AA stranded them

  - Additional $401.40 + $161.25 charges on Max's cards when they said they'd only charge $120 for UM fee

To-do for open sourcing:

- [ ] Planning documents. What's the best format for these? Maybe narrative form?

- [ ] Comb and annotate finances so Bank is ready to open source

  - Flagging now that there are some travel expenses that I (Zach) don't remember us approving

- [ ] Read-only version of ZephyrNET online

## Structure for open sourcing

Four parts to open sourcing:

1. Aggregate planning docs
2. Write-ups:

   - Deploy flow / how the ZephyrNET works
   - Finances / the money behind it
   - How we got the train / train problems / Melody's post

3. Bank transparency mode
4. ZephyrNET read-only mode

### Outline ideas by Zach

Should this be in narrative form? Or maybe just link all the files?

---

Ideation / coming up with the idea

Securing the train (maybe we can share some of the emails we sent and meetings we had?)

The announcement (details around the Slack ticketing system and screenshots from the call we had, including Tom's puzzle)

ZephyrNET / hackathon purpose (and the why behind it. why not just a normal hackathon?)

The schedule / itinerary (ex. the stuff on hack.af/zephyr)

Finances

### Groundhog day

_or, how we put the zephyrnet online after the train and reset it every 24 hours to make sure people don't mess with it even if they still have access_

- Services & websites available on the public internet at *.zephyrnet.hackclub.com
  - Also need a working IP address
- These should be public & searchable
	- zephyrnet.hackclub.com
	- chronicles.zephyrnet.hackclub.com
- Nothing that shouldn’t be shared is shared
	- confessions
	- chronicles
	- photowall
	- media
- Resets every 24 hours
	- Services should spin up all fine
- Bandwidth limiting (sane defaults that don’t hog office wifi)
- Firewalled from office network

Stretch goals

- VPN access to zephyrnet
- analytics (who is browsing zephyr net, what services take the most resources etc.)
- Alert anyone who uploaded their SSH keys to zephyrnet
- Zero downtime reset (spin up a new VM instance before old one goes down)
- custom shutdown message on reboot
- login message updated to mention reboot/reset