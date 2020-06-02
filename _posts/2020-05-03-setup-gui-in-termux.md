---
layout: post
title: "Setup Gui ,vncserver,x11 and desktop environment in termux"
author: kcubeterm
categories: termux
image: https://cdn.jsdelivr.net/gh/hindux/Hindux.github.io/assets/images/Gui.jpg
tags: [ vncserver , GUI ]
description: "Here,how to setup vncserver,desktop environment and Gui in termux,make your terminal fullfilled with gui as well as cli"
rating: 4.5
toc: true

--- 
 This is world of Graphical User Interface, everyone like gui program
 so similar to linux ,termux have also lot's of gui program in the separate repo

#### Subscribe x11-repo 
In order to subscribe the x11 repo ,execute following command in termux
 ```
 pkg install x11-repo 
 
 ```
we always recommend that update repo everytime,but since `pkg` is wrapper of apt ,its automatically update your terminal and then install your packages

#### Requirement
* Vncserver (tigervnc)
* GUI program
* Atleast 100 mb of internet data.(Desktop environment)
* little bit of patience

#### setup vncserver
> In computing, Virtual Network Computing is a graphical desktop-sharing system that uses the Remote Frame Buffer protocol to remotely control another computer. It transmits the keyboard and mouse events from one computer to another, relaying the graphical-screen updates back in the other direction, over a network.

##### why vncserver
 Vncserver is needed here because termux does't support opengles or similar for graphics rendering.
 By the way we can use xorg server also,but thats not stable in android,thats why i choose vnc.Now you have to install an external vncviewer from playstore
 install vncviewer with this [link](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android) .
 
install vncserver 
```
pkg install tigervnc
```
after installed, execute vncserver `vncserver :1` , 
here vncserver is command and `:1` means the vnc server will run on localhost:5901 or 127.0.0.1:5901  


it may ask for password, you just give it any password,which you can remind easily, while putting password your password won't prompt because of privacy.
if your terminal gives output like following,then your vncserver is listening on your specified port.
![vncserver localhost:5901]( /https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/vnc1.jpg)

for knowledge purpose:
sometime you may face issue like following.that time just kill that port, like in following case its is :1 then
`vncserver -kill :1`
![ vncserver ](/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/Localvnc.jpg)

#### setup Desktop environment(xfce4)
There are lots of desktop envirinment for linux like Gnome,xfce4,lxde etc,but termux has only xfce4 available right now.
so install xfce4 by :
```
pkg install xfce4
```
after that set DISPLAY environment variable, on which your gui program interact. if your vncserver run on `:1` then set display on 1,and start xfce4 as well.
```
export DISPLAY=:1
startxfce4
``` 

#### setup vncviewer app.
step 1: Open vncviewer application. and then click on cross + floating button


step 2: fill address and name
![address and name](/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/vncstep2.jpg)

step 3: toggle picture quality on high for best graphics andthen hit connect
![tiggle high ](/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/vncstep3.jpg)

step 4: 
if it ask for password, provide it, if you have forgot your vncserver password,then dont't worry.
come in terminal and change your vncpassword with 
`vncpasswd`


#### script for summarize
```
pkg install x11-repo -y
pkg install tigervnc -y
pkg install xfce4 -y
vncserver -kill :1
vncserver :1
export DISPLAY=:1
startxfce4

```









