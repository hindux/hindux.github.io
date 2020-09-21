---
layout: post
title: "Basic navigation part-II"
description: "Here we discuss about absolute path and relative path in termux,cover $PREFIX and few more things which makes termux different from standard linux."
toc: true
---

#### What we learn now ?

In this tutorial we will interact with text editor, and creating and removing files and directories.



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


After installion let's write something in *file1* which we have created earlier.

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

You can see in line 3 , there is a directory named termux.

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
