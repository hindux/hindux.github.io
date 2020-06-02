---
layout: post
title:  "How to play audio in termux chroot or proot OS like Arch Debian Ubuntu etc"
author: kcubeterm
categories: termux-chroot
tags: [chroot, audio ]
image: https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/audio.png
description: "Here i am going to explain abiut ,how can i play audio in proot environment with pulseaudio server"
featured: true
hidden: true
rating: 4.5
comments: false
---


#### follow now
The term chroot refers to a process of creating a virtualized environment in a Unix operating system, separating it from the main operating system and directory structure. that's why we can use it separtely for many purposes like testings,building etc


Now before doing anything you must have your termux repo updated and pulseaudio installed
for install pulseaudio ,execute following script
```
pkg install pulseaudio -y

```
Now copy and paste follwing command in terminal
```
pulseaudio --start --exit-idle-time=-1
pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1
```

after that make sure you havent get any error.
now open chroot ,i mean your linux which you have installed in termux(smart geek)
and set the pulse server 
```
export PULSE_SERVER=127.0.0.1
```
 your setup has finished ,play audio in linux ,the audio should works.
if that does't work please contact us.


