# Streams

Linux has 3 core *file streams*:
* `stdin`  --> defaults to keyboard (abbrev 0)
* `stdout` --> defaults to screen (abbrev 1)
* `stderr` --> defaults to screen (abbrev 2)

But any of these "hoses" can be redirected to point to a file (this is
possible because, under the hood, Linux represents *everything* to the
user -- even hardware like the monitor or keyboard -- as if it were a
file)

# Redirection operators

```
>                              # redirect stdout to a file (clobbers)
1>                             # same as above
>>                             # redirect stdout to a file (appends)
2>                             # redirect stderr to a file (clobbers)
2>&1                           # redirect stderr to wherever stdout is
                               # (order of redirections matters!)
```

# Pipes

Many Linux commands and utilities are designed to take input from
`stdin` (when not otherwise specified) and sent output to `stdout`
(when not otherwise specified).  The pipe operator `|` is placed
between two commands that sit on a single line (each command gets its
own `stdin` and `stdout` "hose"), and the `stdout` hose of the command
on the left gets plugged into the `stdin` hose of the command on the
right.

For example:
```
$ cat file1 file2 | head | tail
```


## Some useful text filtering utilities that work this way

```
cat
tr
wc
uniq
sort
comm
cut
```

## tee

Lets you redirect while still sending output to `stdout`:
```shell
$ cat file1 file2 | head | tee file1and2.txt
```
What happens?

## `curl` will grab the file at a URL and send it to `stdout` by default
```shell
$ curl <url>
```


## `wget` can send output to `stdout`

`wget` is not installed on Macs by default.  It defaults to sending output to a file, but you can redirect it to `stdout`:
```shell
$ man wget
$ wget -q -O - <URL>
```
`wget` normally gives you lots of output, including a progress bar.  `-q` suppresses this extra output.

The `-O` flag tells `wget` where to send output.  That flag expects a filename argument.  When we give `-` as the "filename", `wget` sends output
to `stdout` (**NB:** -- most text filtering utilities treat `-` as referring to `stdin`; `wget` is anomalous in this respect)

## Declaration of Independence pipeline exercise

This URL [https://www.constitution.org/usdeclar.txt](https://www.constitution.org/usdeclar.txt) contains a plain-text version of the US
Declaration of Independence.  Create a *single* pipeline that gives a list of the top 20 most frequently occurring words in that document, along with their
word counts.  Ignore case, and ignore punctuation of any kind.  Your output should go **both** to the screen **and** to file called `us_decind_top20.txt`.




