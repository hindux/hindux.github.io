---
layout: post
title: "Termux guide for begginers "
author: hindux
categories: [Termux, Termux-tutorial]
tags: [termux]
images: "assets/images/Termux begginer.jpg"
description: "A full explained termux tutorial.This guide helps to any  begginers who want to master termux or any terminal. This guides explains whole concepts of termux like, termux addons, termux bash command, termux api commands and whole whatever termux has."
featured: true
hidden: false
toc: true
next: http://localhost:4000/termux-installation
---
This guide would be dive into the beautiful world of termux and explains all concepts abouts termux and its addon.


#### What is termux ? 
Before going into deep ,we should know that what exactly termux is, Termux is a very powerful linux terminal emulator which runs in android,
> Termux is an Android terminal emulator and Linux environment app that works directly with no rooting or setup required. A minimal base system is installed automatically - additional packages are available using the APT package manager.

Yes, termux is not just a simple terminal , it has own packages, it has above 1000+ packages, that's why popularity are increasing day by day.

#### What is different from standard linux ?
Offcourse it is different from linux in many aspects. As we know linux is OS but termux is just an android application which has to follow android restriction, in order to provide similar linux environment in android. It has all directory in $PREFIX , 
You may know if you have ever run linux  ,linux has /bin,/usr/ ,/share /etc all has in its root directory,but in unrooted device it's impossible to write and execute program in android root directory , so termux has it's own environment.

Here $PREFIX stand for /data/data/com.termux/files/usr/

and all directory in $PREFIX,because any android app can read, write , execute in his /data/ partition

$PREFIX/bin
$PREFIX/etc
$PREFIX/share
$PREFIX/var

for more info I suggest you must visit [termux-wiki](https://wiki.termux.com/wiki/Differences_from_Linux)

#### Termux: addon
So termux has some additional apps also known as "addon", addons fulfill some requirement of termux and adds some more features in termux which usually not find in any android terminal

* Termux:api
* Termux:boot
* Termux:widget
* Termux:styling
* Termux:x11 (upcoming)
* Termux:float
* Termux:tasker

we will disscus more later,for now just intro
##### Termux:api
Termux:api provide commandline access to the device api, termux can send messages,use  gps, wifi access etc.

##### Termux:boot
Termux boot provides functionality if execution of script while booting device,

##### Termux:tasker
Termux task is plugin of tasker which help to execute program or script in termux from tasker app

#### Termux packages
As i mentioned above termux has more than 1000 packages in this repository

let's talk about some popular tools which can make your days.
Termux support some popular  programming languages like

* python
* Ruby
* perl
* Nodejs
* Golang
* php
* Lua
* swift
and have few compiler available which can help you to compile languages like c/c++ and java, it has clang and ecj which can compile c/c++ and java respectively

It has popular webserver ,apache2 and nginx which help you to serve your website from termux.

It has some serious hacking tools 
* metasploit
* Hydra
* nmap
* settoolkit
* aircrack

You will get to know more tools which is available in termux, just stay tuned and open next tutorial.







