---
layout: post
title:  "Setup termux x11 with some simple steps"
author: kcubeterm
categories: termux
tags: [x11,GUI ]
image: assets/images/x11.jpg
description: "setup xwayland and termux:x11 apps in some simple steps, and install termux x11 before release , termux x11 is addon of termux."
featured: true
rating: 4.5
comments: true
toc: true
---
#### What is Termux:x11 ?
As name suggest "X11" it is another addon of termux, which is quite useful when you want to use GUI application like any Desktop environment,this addon did't released yet (20 may 2020) because of some minor issue, i hope it will release soon.


#### Why Termux:x11 ?
Termux:x11 should exist because termux does't support graphics,that's why  in order to use GUI application from termux.


it use wayland protocol and has many advantages over X
for more info, have a look [here](https://askubuntu.com/questions/11537/why-is-wayland-better)

#### Install Termux:x11
Since it did't release yet, even then you can install it,if you have installed you can skip this part


###### Backup your data,
You have to uninstalled all addon and termux app to install it, because right now termux:x11 is not available in playstore or fdroid.
you know that, any if termux application can't be install if signature is different.

```
termux-setup-storage
cd /data/data/com.termux/files
tar -cvzf /sdcard/termux-backup.tgz home usr
```

After executed above command ,just wait..

when you done with it. just learn how you will restore your backup.
```
termux-setup-storage
cd /data/data/com.termux/files
tar -xvzf /sdcard/termux-backup.tgz

```

Above command will help you to restore your backup when you will install new termux.


##### Uninstall stuff
Here i mean, just uninstall all your termux and its addon, make sure all addon means all addon,
* Termux apps
* Termux:styling
* Termux:tasker
* Termux:Float
* Termux:widget
* Termux:api

##### install stuff
Now it's time to install things,I signed all apk with same signature, download it from my [cloud server link ](https://mega.nz/folder/7dggHIKJ#nXq5Gs9BJLdqn4kRmgTkpA)
i signed all apk with apksigner default key, The reason behind it is simple, if any user want to update his app in future then can download from fdroid and sign with apksigner apps availabe in playstore.
[apksigner link](https://play.google.com/store/apps/details?id=com.haibison.apksigner)
That's why i didn't sign with any terminal tool.
##### Termux:api SMS
If you want to enable sms features in termux then you can download termux api with above link or [cloud server link ](https://mega.nz/folder/7dggHIKJ#nXq5Gs9BJLdqn4kRmgTkpA)
This termux api is latest version and recompiled in order to get sms features

##### Restore your backup now
I have mentioned above,
#### Setup X11 now
just execute following command in your terminal
```
pkg install x11-repo
pkg install termux-x11
pkg install xwayland
termux-x11
```
After that retun in terminal(termux)
open new session and export DISPLAY

```
export DISPLAY=:0
```
Now if you have any gui application or any Destop environment installed, 
start it. In my case I start xfce4, if you want to install it, `pkg install xfce4`
```
startxfce4
```
Go to termux:x11 apps and enjoy your gui.

If you face any type of issue , contact me: kcubeterm@gmail.com or open issue on [github](https://github.com/termux/termux-x11/issues)



