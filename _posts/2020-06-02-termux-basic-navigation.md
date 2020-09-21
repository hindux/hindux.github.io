---
layout: post
title: "Basic navigation in termux commandline"
description: learn basic navigation in termux,know about command like ls, pwd,cd,rm etc.
comments: false
nxt:
prev:
toc: true
---
In this tutorial we'll learn the basics of navigation or moving around termux directory.

#### print working directory(PWD)
when you open termux commandline,do you know where you are ?. In which directory you are ?
So in order to knowing the current directory. The command `pwd` come into play

execute `pwd` in termux
```
$pwd
/data/data/com.termux/files/home
```
command `pwd` gave output `/data/data/com.termux/files/home`

`pwd` always help you when you forget where are you ?

#### list(ls)
The next command is `ls` ls stand for list, as name suggest "listing". So command `ls` is used for listing files and directory in your current path or specified path.

execute `ls` in your commandline.

```
$ ls
storage
kk
termux.txt
```

if it does't show anything, it means, your current directory contain nothing or files are hidden.

In linux/termux the files or directory  which has dot in prefix like `.termux`  won't listing with `ls`. Here you have to use `-a` option.


##### Listing hidden files
As you know the files which contain dot in starting that's cannot be visible by just `ls ` command, here we shiuld use `ls -a`

for example, create two file with or without dot .
use `touch` command to create files


```
$ touch .hidden
$ touch visible
ls
visible storage
```
In above example we created two file , first one is ".hidden" and second one is "visible"
and when we execute `ls` visible shows but .hidden dont.

Now use `ls -a` to listing  all files and dirrctory
```
$ ls -a
. .. .hidden storage visible
```

you can see above `ls -a ` listed all files and directory.

#### List file permissions

Files and directories permissions can be list by `ls -l` and `ls -a`

```
$ ls -l
total 4
drwx------ 2 u0_a290 u0_a290 4096 Jun  3 11:40 storage
-rw------- 1 u0_a290 u0_a290    0 Jun  3 11:39 visible

```

For viewing hidden file permissions as well use `-a` flag with `-l`

```
total 24
drwx------  3 u0_a290 u0_a290  4096 Jun  3 11:40 .
drwx------ 99 u0_a290 u0_a290 16384 Jun  3 11:39 ..
-rw-------  1 u0_a290 u0_a290     0 Jun  3 11:39 .hidden
drwx------  2 u0_a290 u0_a290  4096 Jun  3 11:40 storage
-rw-------  1 u0_a290 u0_a290     0 Jun  3 11:39 visible


```

**We'll know more about file permissiins further**


##### Clear terminal.
you have already filled your terminal .let's clear it by command `clear`.

just execute command clear in your terminal and magic will happen.


#### playing with directories.
Directories in termux, when we open termux the default directory is  home directory.
But suppose you want to go in your internal storage or any other directory.

Here command `cd ` help us, cd stands for change directory.
change your directory into /sdcard

like execute `cd /sdcard` and then execute `pwd`

Here before changing your directory into /sdcard. you have to give storage access permission to termux.

execute `termux-setup-storage` and after prompting window permit it.

```
$ cd /sdcard/
$ pwd
/sdcard
```
Now we should learn about some tips so that navigating between directories will be more convenience.

* `~` (tilde) represent home directory, no matter where you are, whenever you execute `cd ~`
	you will return in home directory
* . (dot) - This is a reference to your current directory.

* `..` double dot represent parent directory or one directory up.


Now suppose you are in /sdcard directory. if you want to return home directory. execute `cd ~`
```
$ pwd
/sdcard
$ cd ~
$ pwd
/data/data/com.termux/files/home
```

Now suppose you are in `/data/data/com.termux/files/home` directory and want to go one directory up
in ` /data/data/com.termux/files` so simply execute `cd ../` or `cd ..`

```
$ pwd
/data/data/com.termux/files/home
$ cd ..
$ pwd 
/data/data/com.termux/files
```
#### What's next 
The next tutorial will be on removing and creating files and directory.



