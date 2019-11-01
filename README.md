# More Command Line Tools

## This workshop

[https://github.com/gabeclass/cmdline_tools](https://github.com/gabeclass/cmdline_tools)

## About
These are reference materials for the PiCSciE workshop **Command Line Power Tools** at Princeton. 
This workshop assumes a modicum of prior experience with Linux/Unix systems and specifically the bash shell, including the basics of redirection. The goal is to expose people to additional command line tools beyond those used for simple navigation of the filesystem and operating with files and directories.

## Adroit
The workshop requires access to a Linux system and a shell. Mac users using the shell that comes with macOS should be ok, but since there can be some differences between the operation of some commands in Linux systems and on macOS, it's ideal if you've installed the GNU versions of standard command line utilities using a package manager (e.g. Homebrew). Windows users can get a local Linux shell using the Windows Subsystem for Linux or some other add-on like Cygwin.

Alternately, participants can do all the exercises by SSHing into Princeton's Adroit cluster.  Note that in order to connect to Adroit, you must be on the Princeton **eduroam** network (the **puvisitor** network will *not* allow a connection to
Adroit), and you must be able to Duo authenticate. If you were off campus, you would need to establish a connection to Princeton's VPN first. OIT has
[instructions](https://princeton.service-now.com/snap?id=kb_article&sys_id=ce2a27064f9ca20018ddd48e5210c745)
for how to do that.

<!-- You can find the page, presentation and examples either in the
[src/](src/) folder or hosted via Github Pages at
[https://princetonuniversity.github.io/hpc_beginning_workshop/](https://princetonuniversity.github.io/hpc_beginning_workshop/)
-->

## **WARNINGS!**


* **Linux is _case-sensitive_** (macOS may or may not be, depending on
  how your hard drive's filesystem was configured).

* **The command-line is _unforgiving_!** Type things *EXACTLY* as you
  see them, and avoid interpreting (and don't assume the computer will
  interpret anything for you -- be precise).


## For one of our exercises

The URL below takes you to a plain text version of the US Declaration
of Independence:

[https://www.constitution.org/usdeclar.txt](https://www.constitution.org/usdeclar.txt)

## Instructions for setting up SSH keys (passwordless SSH)

[Set up SSH keys](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-on-ubuntu-1604)

## Google Survey
Near the end of the workshop, you'll be asked to fill out a brief (3-5
mins) survey. When the time comes, please
[click here](https://forms.gle/WhoAcb1J82XVTqq38).

<!--
## Resources for further study

* _The Linux Command Line_ (a book by William Shotts -- [free PDF
online](http://linuxcommand.org/tlcl.php)

* _Introduction to Linux: A Hands on Guide_ (a book by Machtelt
  Garrels -- free PDFs discoverable online; [full HTML
  version](https://www.tldp.org/LDP/intro-linux/html/) is online)
  
  
* Afternoon session (Intro to HPC on the Princeton Clusters)

* Wednesday session (Command Line Power Tools -- moves faster, a bit
  more advanced, but worth seeing even if you can't keep up this time
  around)
-->
<!-- [Getting Started with
HPC at
Princeton](https://researchcomputing.princeton.edu/education/online-tutorials/getting-started)
--> <!-- [OnComputingWell](https://oncomputingwell.princeton.edu) -->
<!-- [Research Computing
FAQ](https://researchcomputing.princeton.edu/faq) --> <!--
[AskRC](https://researchcomputing.princeton.edu/about/contact/ask-research-computing)
-->

## Getting Help Later

If you encounter difficulties working on the PU computing systems or
have basic Linux questions, please drop in to one of PICSciE's twice
weekly <a
href="https://researchcomputing.princeton.edu/education/help-sessions">live
help sessions</a>, visit our blog
[*OnComputingWell*](https://oncomputingwell.princeton.edu) to see if
someone has answered your question, post your question on our Q&A site
[AskRC](https://researchcomputing.princeton.edu/about/contact/ask-research-computing),
or send an email to <a
href="mailto:cses@princeton.edu">cses@princeton.edu</a>.

<!--
## About Makefile
I update the documentation directory using a Makefile to sync src/ and docs/, with
the 'Dinky' theme because its seemed apropros of Princeton. To run it, just run
`make` from the repo root.
-->

## Authorship

This workshop was prepared by Gabe Perez-Giz. It incorporates some
elements from an earlier incarnation of this workshop by Ben Hicks and
borrows some pieces from Jonathan Halverson.
