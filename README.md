# fotobot
a photo robot

# what is fotobot?
here is a vimeo video that explains the basic premise: https://vimeo.com/60848065

# wait, so it already exists?
yeah kind of. we built a super hacky version of it a couple years back for a friend's wedding. since then, lots of folks have asked to use it, so I want to build something more stable. a webservice, perhaps.

# the process
for a user:
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
5. repeate until ending time is reached
