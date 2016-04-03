# ImgurFox

A Firefox extension originally made by Chromakode and koryk to upload images to imgur.com

The extension was on the firefox addons website and was updated until
the end of 2015 when it was removed. The original repo did not contain
the updated sources and couldnt be used to build the xpi available on
the firefox website. I've extracted the modifications from the .xpi
installed on my system and applied them to the repo.

# TODO

imgur has removed support for the v2 API which means the addon doesn't
work anymore. I suspect it's the reason why it was also removed from
the store.

From what I've seen on the imgur API documentation[1], the v3 API
hasn't changed much as far as uploading images is concerned. It looks
like it might work as-is by just updating the api url from "/2/" to
"/3/" (hm.. have to check if the returned objects have the same format maybe too).

The main problem is the OAuth thingy which must be updated to OAuth v2
(currently v1).

There's an example gist in the doc to do that [2].

1: https://api.imgur.com/
2: https://gist.github.com/eirikb/7404666
