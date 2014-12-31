# Programming Tools and Techniques.

This repository will contain all the material relevant for the
Programming tools and techniques course.


## How to contribute?

You can fork this repository on bitbucket and send pull request. Make
sure that your patches have sane author name and email id. You can set
these once and for all using the following command.

```bash
$ git config --global user.name "Piyush Kurur"
$ git config --global user.email ppk@myhost.mydomain

```

Also make sure that your patches do not have trailing spaces and
newlines. Easy to get this operational is to set your pre-commit hook.
This will disallow you from committing patches that have a trailing
space or trailing set of newlines.

```bash

$ mv .git/hooks/pre-commit.sample .git/hooks/pre-commit

```
