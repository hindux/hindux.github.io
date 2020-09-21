---
layout: post
description: "How to install packages in termux, getting info about packages, find packages of his/her choice"
toc: true
comments: false
hidden: true
categories: Termux-tutorial
---

In this we will learn "How to install packages in termux", not only installation, will cover listing, removing and searches also.


#### List help for pkg
execute `pkg help` in your terminal to listing all subcommand.



#### How to install packages.

As you know termux has own packages and package manager also.

In order to install packages in termux , we will use `pkg`

**Warning: Don't use apt for installing packages in termux.**

we will prefer only pkg for installing packages.

let's install nano text editor again.
`pkg install nano`

Above command will ask for confirmation, just hit enter to proceed.
in case if you want confirmation in one liner. use `-y` flag like 

`pkg install nano -y`

#### How to remove packages

In order to removing packages use remove subcommand.

`pkg remove PACKAGE_NAME`

e.g lets remove **nano** then
`pkg remove nano`

##### Searching packages.

we can search packeges by keywords, like suppose I want packages which can play music.
so we can search **music** keyword.

`pkg search music`

its gives you available packages which contains music in his metadata.

Lets take one more example.
I want packages related to web terminal.

`pkg search web terminal`

above command looking for all packages metadata which contain both keyword in same package.
So whatever you result you will get, will see that package contain both keyword, **web terminal**

You will get same list with this command also

`pkg search terminal web`


But once you quote multiple keywords, you will get exact matches.

like `pkg search "web terminal"` and `pkg search "terminal web"` is different.


##### Get package info

pkg provides a subcommand `show` which is used for getting few info about that specifice  package.


let's list info of micro text editor.

`pkg show micro`

There are few more subcommand which is quite useful. you can list via `pkg help`


#### What is next ?

