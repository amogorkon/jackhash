# JÄCKhash - Japanese, ASCII (+non-latin), Chinese, Korean Hash encoding
Ever felt sha256 hexdigests are way too long? We have unicode everywhere now, right? Why not use the full range of characters of unicode to encode the hash?
Well, there are some potential issues to take into consideration.

Many characters in ASCII have special meaning to a machine, which potentially breaks highlighting. Emojis are especially troublesome due to interoperability - many editors, chat clients etc. don't display the same emoji in the same way, some even expand the emoji to a :text:, which defeats the whole purpose of compressed encoding.
However, the chinese, japanese and korean alphabets are *huge* in comparison, yet don't come with any of these downsides - editors, chat clients etc. all seem to display these characters the same way and there is no special meaning assigned to any of these characters by machines, so they are handled properly as one big string, easy to highlight and copy&paste.

I curated all those different alphabets into one (japanese would only add 100 single characters to the chinese and korean alphabets and the license would be GPL3, so I left that one out actually) - coming up with a combined alphabet of 27642 characters, which allows to boil down the length of a sha256 digest down to just 18 characters which you can freely send via chat or put in Python 3 code files since they are unicode by default.

## Licensing
Both Chinese ( https://github.com/tsroten/zhon/blob/develop/zhon/cedict/all.py ) and Korean ( https://github.com/arcsecw/wubi/blob/master/wubi/cw.py ) alphabets are licensed under MIT
