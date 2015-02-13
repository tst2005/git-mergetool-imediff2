# imediff2 support for git mergetool

A first script to be able to use imediff2 in the git merge steps.

# My needs

I searched a simple command line (ncurses) util to be able to solve merge problem without graphical dependencies (usualy on remote server).

I need a simple and friendly util without spend time to learn how to use it.

# I found imediff2

It's simple to use, arrow keys, tab, enter, ... perfectly simple !

You can install it, on debian with `apt-get install imediff2`.

# Not supported by git

Unfortunately it was not supported by git.

My current debian stable version of git was the 1.7.10.x

In /usr/lib/git-core/mergetools/ 
 * araxis
 * bc3
 * defaults
 * deltawalker
 * diffuse
 * ecmerge
 * emerge
 * imediff2
 * kdiff3
 * kompare
 * meld
 * opendiff
 * p4merge
 * tkdiff
 * tortoisemerge
 * vim
 * xxdiff

I wrote a simple [imediff2](https://github.com/tst2005/git-mergetool-imediff2/blob/master/imediff2) script to support it.

# How to use it

I put my script inside the system directory :

## Install the script
```
cp -a imediff2 /usr/lib/git-core/mergetools/
```

## Configure your git to use it

```
git config --global merge.tool imediff2
```

# Limitation

imediff2 only support 2 files merge, So the 3 files compare is not supported.


