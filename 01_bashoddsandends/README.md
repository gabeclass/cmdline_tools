# Fetch some remote files

Make a folder in your home directory titled `powertools`.  `cd` into
it, and then fetch [this
file](https://web.math.princeton.edu/~perezgiz/sec1.tar.gz).  Untar it.

# `for` Loops

Bash has `for` loops.  They operate as `for each` loops, iterating
over sequences (i.e. like Python loops), *not* numerical C-style loops
(those are doable in `bash`, but they aren't so common).

## Syntax

Say you want to loop over the files in the current folder and `echo`
each one followed by `"is a file"`.  The syntax is multiline (you'll
get the secondary prompt as you go), or you can do it on a single line
with semicolons (if the `do` part has many statements, put each on its
own line, or its own semicolon-separated chunk of your single line):

``` shell
$ for j in *
> do
> echo $j is a file
> <other statements>
> done
```
OR
``` shell
$ for j in *; do echo $j is a file; <other statements>; done
```

## Exercise

Make a new folder called `barnyard`.  Take every `.jpg` file in
`haystack`, and copy it into `barnyard` but changing the extension to
`.JPEG` (the `basename` command may be useful -- `man basename`)



# String substitution

Bash can take the output of a command and put it into something that
is treated as a string variable:

``` shell
$ x=$(ls haystack/*.jpg)
# Compare that to...
$ y="$(ls haystack/*.jpg)"
```

# Process substitution

Bash can take the output of a command and put it into something that
is treated as a *file* (useful for commands that expect file
arguments):

## `diff`

(And let's learn about the `diff` command while we're here...)

``` shell
$ diff <(command-1) <(command-2)
# Look for the -u flag of diff.  Gives output similar to what git does by defaultq
```

To *write* to a command as if it were a file, use `>()` (this can be
combined usefully with, e.g., `tee`)
