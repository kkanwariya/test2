% Getting started
% Piyush P Kurur
% January 5, 2015

# Getting started

## Machine lab and all that

- *Three* of you will have a lab machine.
- Get yourself a personal machine
- Have one of your favourite Unices on it (GNU/Linux or *BSD)


## Prerequisites

- One of vim or emacs (my preference)
- Basic usage of computers, command prompts etc.
- Know about man pages and google.

## General Advice for being a hacker.

- Use terminals for interaction
- Use applications like tmux and screen

# Todays topic: Git and Bitbucket.

## Git and Bitbucket, what are they?

- Git is a *Distributed Version controller*
- Helps you keep track of a changing set of files.
- Bitbucket hosts git (and mercurial) repositories.

## Bitbucket accounts

- You must create an account  (visit <http://bitbucket.org>)
- Get Academic accounts (just use cse.ac.in id)
- Has a lot of nice features like unlimited private repo.

## Goodies on bitbucket

- [Source of slides, code examples etc][repo]
- [Course wiki][wiki]
- [Issue tracker][issues] for issues and discussion.
- Assignments should be in private repos there.


# Coming back to git

## What is git?

- It is a Distributed version control system (DVCS)
- Written by Linus Torvalds and is used by the Linux Kernel
- Very popular.
- You can host stuff on sites like bitbucket and github.

## Name and Email

```bash

$ git config --global user.name "James Bond"
$ git config --global user.email '007@mi6.uk'

```
. . .

### Exercise

What if `--global` is dropped?

## Start giting


> - Initialising

```bash
$ cd /your/project/dir
$ git init
```

> - Clone

```bash
$ git clone git@bitbucket.org/ppk-teach/tools
```
(This is to be done only after ssh key is set up. Other wise  use

```bash
$ git clone https://amartya20x@bitbucket.org/ppk-teach/tools.git
```

## Every repository is first class

- There are no "centralised store"
- Changes/patches are *pushed* or *pulled* into repositories


## Some Git terminologies.

### Repository

- Stuff that has been kept track of
- History commit messages etc

### Working copy

- The latest stuff.
- Can contain modifications to stuff in repository
- Some untracked files.

###  Working copy to repository

- Stage stuff: new untracked file or modification of tracked file.
- Commit: Added the staged stuff to the repo


## In command line.

```bash
$ git add README.md  # This stages the file for commit
$ git commit # This will start an editor to record commit message'
$ git commit -m 'Added a readme'
             # -m sets the one line commit message
			 # no editor is started.
$ git commit -a README.md -m 'added a readme'
$ hack hack hack
$ git commit -am 'more detailed install process in readme'
           # Added all the modifications to tracked files and commit
```


### Exercise

Which is the editor started for commit? How can one set it?


## Branches.

```bash
$ git branch      # See branches
* master          # Only one branch master and you are on it
```
. . .

```bash
$ git branch topic   # Create a topic branch
$ git checkout topic # Move to topic branch
$ git branch
  master
* topic
$ do stuff on topic
$ git checkout master # move back to master
$ git merge topic     # merge the changes to topic
```

### Pushing and pulling


```bash
$ git push  # Send our changes to upstream
$ git fetch # get changes but do not merge
$ git pull  # fetch and merge.
```

- pull = fetch + merge

- safer to use fetch, review mer



## Remote repositories.

- What if you want to work with multiple repositories.
- You can define remote repositories.

## Example workflow.

```bash
$ cd code/git/raaz
$ git remote -v
  abhijaju        https://github.com/abhijaju/raaz.git (fetch)
  abhijaju        https://github.com/abhijaju/raaz.git (push)
  build   ppk@ppk.cse.iitk.ac.in:code/git/raaz (fetch)
  build   ppk@ppk.cse.iitk.ac.in:code/git/raaz (push)
  ...
  origin  git@github.com:piyush-kurur/raaz.git (fetch)
  origin  git@github.com:piyush-kurur/raaz.git (push)
  ...
  upstream        git@github.com:raaz-crypto/raaz.git (fetch)
  upstream        git@github.com:raaz-crypto/raaz.git (push)

$ git fetch abhijaju/master      # Bring abhimanyu's changes
$ git checkout abhijaju/master   # See his snapshot.
# review the changes
$ git checkout master            # Back to master
$ git merge abhijaju/master      # Looks good so merge.
$ git push origin                # Send it to my fork on github
$ git push upstream              # Send changes to upstream
	                             # Yeah I am the king here.

```

## Summary

- Start with `init` or `clone`
- add new files with `add` or stage them
- hack, `push`, `fetch`,
- `branch`, `merge`z.

## More information

- Comprehensive Documentation <http://git-scm.com/documentation>
- Millions of tutorials on web.

## Some tools I use

- tig - a git changes browser.
- magit - An emacs mode for working with git.
- gitk - a graphical git browser that I rarely use.

# Tailpiece : SSH Keys

## SSH without passwords

- Use public key authentication
- Multiple users without sharing passwords
- Multiple hosts with the same public key

## SSH key generation

```bash
$ ssh-keygen
$ ls $HOME/.ssh/
...
id_rsa      # Private key (keep it safe)
id_rsa.pub  # public key  (upload on bitbucket)
```

More details on my [blog on key based access][ssh-blog]


[repo]: <http://bitbucket.org/ppk-teach/tools> "Source Repository"
[wiki]: <http://bitbucket.org/ppk-teach/tools/wiki> "Course Wiki"
[issues]: <http://bitbucket.org/ppk-teach/tools/issues> "Course Wiki"
[ssh-blog]:
   <http://cse.iitk.ac.in/users/ppk/posts/2011-06-02-SSH-A-quick-guide.html>
