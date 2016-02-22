# fotobot
a photo robot

# what is fotobot?
fotobot is a live printing rig that pulls photos from instagram. here is a vimeo video that explains the basic premise: https://vimeo.com/60848065

# wait, so it already exists?
yeah kind of. we built a super hacky version of it a couple years back for a friend's wedding. since then, lots of folks have asked to use it, so I want to build something more stable. a webservice, perhaps.

# the process
for an event guest:

1. take a photo at an event
2. add the event hashtag
3. pickup your photo!

for an event photog:

1. login to fotobot admin
2. define the target hashtag
3. select the delivery method (Dropbox or Google Cloud Print)
4. select an ending time
5. monitor the printing during event

for the script itself:

1. when given a hashtag, poll Instagram for photos every X seconds
2. when a new photo is found, pull the image, user, and caption
3. plug image, user, and caption into a template
4. send resulting file to selected Dropbox or Google Cloud Print printer
5. repeat until ending time is reached

# why build this?
a couple of reasons:

1. it's a blast to setup and run for friends and family
2. it's a free ticket to any tech event in town
3. commercial alternatives can run over $5000/day

# why Dropbox?
a lot of event photographers already have "hot printing" setup and ready to roll. there are a number of professional solutions that simply watch a folder and print any file that lands inside (usually from a tethered DSLR).

# why Google Cloud Print?
a lot of printers now support Google Cloud Print, which lets you send print jobs directly from the cloud via simple API. even if your printer doesn't directly support Google Cloud Print out of the box, you can tether to a computer and magically make it so.

# requirements 

* simple front-end for starting/stopping the bot
* auth / user accounts for controlling access to the bot
* abilty to run multiple fotobots concurrently (ie different events across the globe)

# future features

* twitter support
* simple moderation, where the event photog can watch submissions in the front-end, and yes/no each image before print
* micropayments per photo delivered and printed
