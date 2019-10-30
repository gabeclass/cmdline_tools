## `sed` (the stream editor)

`sed` allows you to make linewise changes to file contents as they soar through `stdout`, letting you modify the contents "in transit",
and then letting you put the resulting transformed output someplace else (including overwriting the original file).

## Tutorial with the basics

Digital Ocean has [a nice tutorial on the basics](https://www.digitalocean.com/community/tutorials/the-basics-of-using-the-sed-stream-editor-to-manipulate-text-in-linux).

## Googling `sed` one- or multi-liners

We all have to google cute `sed` tricks that do what we want.  The important thing is having enough literacy to understand what
Google returns and to cobble things together, enough `sed` literacy to know what's generally possible.


## Exercise

* First, grab a plain-text version of the complete collection of Shakespeare's sonnets (with a bunch of preamble content):
[https://archive.org/stream/shakespearessonn01041gut/wssnt10.txt](https://archive.org/stream/shakespearessonn01041gut/wssnt10.txt)

* Show every line that contains 'beauty' (this is a `grep` move)  (Should we ignore lines from the header/preamble?  How could we do this?)

* Find every line that contains 'beauty' and, if it's intended, unindent it, and save just those lines to a file `beautylines.txt`.

* The last two lines of every sonnet are indented.  Let's produce a full copy of the collection in which that isn't true.


