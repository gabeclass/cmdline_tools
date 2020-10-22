## `find`

`find` is a powerful utility that recursively lists all files and folders starting from the location you pass as its first argument
(and it operates recursively through subdirectories).  Output goes to `stdout`.

There are *many* flags and options:
```shell
$ man find
```

## Telling `find` what you're looking for

Here's a few ways to steer `find` toward what you want (not mutually exclusive):

### Folders vs files

* The `-type` flag, followed by `f` or `d`

### Filename patterns (including globbing)

* The `-name` or `-iname` flag (former is case-sensitive, latter is case-insensitive),
followed by a pattern **enclosed in single quotes!** (so the shell won't prematurely expand it)

### Regular expressions

* The `-regex` flag -- more on this shortly


## Exercises

Make a directory called `findpractice` in your home folder.  `cd` into that directory and execute the following commands:

```shell
touch readme.txt
mkdir src
mkdir lib
touch src/main.py
touch src/main.pyc
touch lib/other.py
touch lib/other.pyc
touch lib/stuff.py
touch lib/foo.py
touch lib/foo.pyc
```

Starting from the `findpractice` folder, write `find` commands that will:
* Find only those files with the `.py` extension
* Find only those files *without* the `.py` extension
* Delete only those files with the `.py` extension
* Delete only those files *without* the `.py` extension

**Useful `find` flags for this:**
`-name`
`-not`
`-delete`

Now add a file called `watchout.py` in the `findpractice` folder (use `touch`).  Repeat the above.  Do the commands you used previously still work?

## Run commands on the files you find

* The `-exec` flag can be followed by any `bash` command.  Put in `{}` within that command in places where a filename would be expected,
and `find` will substitute each file/folder it locates earlier in turn.

* You must put an escaped semicolon `\;` at the end of the command to indicate to `find` that this is where the command ends.



### Example/

* Make three directories within your home folder called `dirtokill1`, `dirtokill2`, `dirtokill3` (play golf! -- Can you do this in one line?)
* Make a directory called `temp` in your home folder, and inside that directory, put three files also called `dirtokill1`, `dirtokill2`, `dirtokill3`.
* Write a `find` one-liner that, departing from your home directory, would find just the aformentioned *folders* and delete them while leaving the eponymous *files* intact.


## Exercise

How would you copy 1 file to multiple directories, in 1 line?  Try to
think of a way to do this with `find` (HINT: consider the `-exec`
flag)
