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

### Hidden files?

* Use the `-a` flag (just like with `ls`)

## Exercises

* Find every folder on Adroit called `.ssh`
* Find every file on Adroit whose name starts with `.bash`  (there are a lot) -- you may want to pipe output to `less`

## Run commands on the files you find

* The `-exec` flag can be followed by any `bash` command.  Put in `{}` within that command in places where a filename would be expected,
and `find` will substitute each file/folder it locates earlier in turn.

* You must put an escaped semicolon `\;` at the end of the command to indicate to `find` that this is where the command ends.



### Example/

* Make three directories within your home folder called `dirtokill1`, `dirtokill2`, `dirtokill3`
* Let's write a `find` one-liner that would find just these folders and delete them.



