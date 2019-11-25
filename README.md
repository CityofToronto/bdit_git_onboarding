# BDITTO Git Onboarding Exercises

This repository contains a few introductory guided exercises for BDITTO members
who are new to Git.  It's complementary to the team's Notion.so onboarding
documentation.

## Setting Git up

### Installing Git

Your workstation will likely already have Git installed.  If not:

For Windows users, your options include:

* Install [Git for Windows](https://git-scm.com/download/win) - download the
64-bit version.
* Installing [Anaconda](https://www.anaconda.com/distribution/) to get Python
and R will also install Git.  Git can then be accessed through the Anaconda
command prompt.
* Installing [PUTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
to [connect to the EC2](https://github.com/CityofToronto/bdit_team_wiki/wiki/AWS)
will also install Git (operating on MINGW).
* Install Windows Subsystem for Linux, then install Git within WSL (using the
Ubuntu procedure below). See the team's guide for installing WSL [here]
(https://github.com/CityofToronto/bdit_team_wiki/wiki/Windows-Subsystem-for-Linux).

For Ubuntu users:

* Run `sudo apt install git`.

For MacOS users:

* Install [Git for Mac](https://git-scm.com/download/mac).

[GitHub Desktop](https://desktop.github.com/) is also available as a GUI
application for Windows and Mac, but because of OS and command limitations, is
not recommended as a substitute for learning the command line.  Installing
GitHub Desktop also installs Git, and enables command line operations.

### Connecting to GitHub

Due to our corporate firewall, connecting to GitHub requires a few additional
setup steps, especially if you're using [two-factor authentication](
https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)
(which you should be). See the Starter Package or Team Wiki for instructions,
or ask a fellow BDITTO member.

### Customizing Git

Finally, set your username and e-mail address:

```
git config --global user.name "Example Name"
git config --global user.email "email@example.com"
```

If you don't wish to publicize your e-mail, you may use a [GitHub `noreply`
e-mail instead](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address).

You can optionally also set up a custom text editor using

```
git config --global core.editor "YOUR EDITOR'S NAME"
```

On Ubuntu and MacOS you can just use the editor's name.  For Windows you may
have to include the entire path to the editor (eg. `"C:/Program Files (x86)/Notepad++/notepad++.exe"`).


## Exercises

Any text in commands that are surrounded by angled brackets `<`, `>` should be
replaced when you type them.

## Exercise 1 - download this repo

**Your first task is to download this repo to your computer.**

1. Click the "Clone or download" button, and "Clone with HTTPS".  This will
copy a web address to your clipboard.
2. On the Git command line, type `git clone <HTTP ADDRESS>`, where `<HTTP
ADDRESS>` is the web address you just copied.  This will download your repo to
your current folder.
3. Navigate to your folder.  You should see the contents of the repo.

## Exercise 2 - create a new branch, and a new commit to it

**Next, create a new branch, and commit a change to Roster.md.**

1. Type `git checkout -b <YOUR BRANCH NAME>`.  `git checkout` is the command to
switch between branches and commits; `-b` creates a new branch.

2. In the text editor of your choice, open `Roster.md` and add your GitHub
username to it.

3. Save your changes to a new commit.  First tell Git to flag all your
changes to be saved with `git add -a`.  Then save these changes to a snapshot
using `git commit -m "<YOUR COMMIT MESSAGE">`.  Make sure your commit message
is meaningful!

3. Try `git diff master`, which compares your most recent commit to the the
most recent commit of `master`.  To quit the diff, press `q`.

## Exercise 3 - push your changes to GitHub, and create a pull request

**Next, let's upload your changes to GitHub and request they be merged with
master.**

1. Type `git push -u origin <YOUR BRANCH NAME>`.  This will copy your branch to
GitHub (`-u` tells Git to track any differences between your computer's copy
of the branch and GitHub's).

2. Go to GitHub, and start a pull request.

## Exercise 4 - address review comments

**Redo the above steps to make changes to your code in response to the
reviewer.**

## Exercise 5 - update `master` from GitHub

