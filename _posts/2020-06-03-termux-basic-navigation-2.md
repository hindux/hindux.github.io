---
layout: post
title: "Basic navigation part-II"
description: "Here we discuss about absolute path and relative path in termux,cover $PREFIX and few more things which makes termux different from standard linux."
toc: true
comments: false
categories: Termux-tutorial
hidden: true
---

#### What we learn now ?

In this tutorial we will interact with text editor, creates ,removes, copy , move and renaming  files and directories.



#### Create a blank file

Let's create blank file with `touch` command. we have already used this command.

```
$ touch file1
$ ls
file1
```

#### Create and write in file.

Now we will use an interactive text editor. There are lots of text editor in termux

List of few text editor
* Vim
* Emacs
* micro
* nano 

Let's use micro editor because it's more suitable for begginers.

Install it by pkg

`pkg install micro -y`


After installation let's write something in *file1* which we have created earlier.

Now open that file with micro like

`micro file1`

afterthat write something. Just write your name and save it by ctrl+s and exit with ctrl+q

Once you saved and exit. You can reopen that file in same way like you did before.
`micro file1`

#### Create Directory

In order to create directory we use `mkdir ` command.

let's create a directory named *termux*, 
```
$ mkdir termux
$ ls
file1 termux
```
#### Copy files and directories.

We will use `cp` commamd to copy files and directories.

##### copy files

let's create an empty directory first.

`mkdir empty-dir`

```
$ mkdir empty-dir
$ ls
file1 empty-dir termux
```

you can see in line 3,

now lets copy **file1** into **empty-dir** 

`cp file1 ./empty-dir`

NOTE: ./ represents current directory, and you know **empty-dir** exist in current dir.

Now after executing above command let's list empty-dir to see that file1 copied or not.

For list **empty-dir**, execute `ls empty-dir`

```
$ ls empty-dir
file1
```

You can use cp to creating dublicate of file.

Here, creating dublicate of **file1**

`cp file1 file2`

The file2 will contains same things whatever file1 contains because file2 is dublicate of file1.Open both file for confirmation.

#### Copy directory

`cp` is use for copying directory also.

Here `-r` option come into play.
-r stands for recursive.

**synopsis** : cp -r Dir DESTINATION_DIR_PATH

e.g. Copy empty-dir into termux

`cp -r empty-dir ./termux`

Above command will copy empty-dir into termux directory, both are exist in current directory.

In order to confirmation , list termux dir `ls termux`

#### Moving file.

Moving files means 


#### Removing files and directories.

we use `rm` command to deleting files and directories.
##### removing files
In our current directories. There is one file and directories.

```
$ ls
file1 termux
```

Just use **rm FILENAME** to delete it.
Here you can use path also to deleting files, if thats not in current diretories.


```
$ rm file1
$ ls 
termux
```

You can see after executing `rm file1` , there's no filename file1 in current directory.

##### Removing Directories.

We can  use same `rm` command for removing directory also, but there for removing directory there is a similar command `rmdir`.

Lets remove directory with `rmdir`

```
$ rmdir termux
```

Above command has removed termux. Here since termux directory is empty that's why it has removed.

##### Removing non-empty directory.

Here we use `rm` with `-r` option.

-r stands for recursive.

So when directory is not empty we will use `rm -r DIR_NAME`




#### What's next ?

We will cover about termux package manager in next tutorial.
