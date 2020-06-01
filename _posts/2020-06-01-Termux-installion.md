---
layout: post
title: "Installion of Termux and it's addon"
description: "This guide explains about how to install termux apps and its addon lime termux api without any errors and tell that what are sources of errors while installing termux apps"
author: kcubeterm
categories: Termux-tutorial
featured: false
hidden: true
toc: true
nxt:
prev: termux-tutorial-begginers
---
This guide is going to explains about termux installions as well as it's addon(termux-api,termux boot etc)

So i don't think installing process of any android application to be tough, just you have to keep somethings in mind that don't mix apk from anothers sources like you install termux apps from playstore and termux api from fdroid or any another sources,

Termux application officially published on Google playstore,Fdroid and kalinethunter store
#### Install from Google playstore
1. Login to your Google account, if you are not already logged in,
2. Open Google Play Store on your Android device by tapping [this link](https://play.google.com/store/apps/details?id=com.termux)
3. Tap Install,
4. Allow the installation to complete,
5. Once installed, you will see the Termux launcher on your home screen and in your App Drawer. Tap the icon to fire up the application.


#### Install from Fdroid
1. Open F-Droid on your Android or Chrome OS device by tapping [this link](https://f-droid.org/repository/browse/?fdid=com.termux),
2. Tap Download APK,
3. Tap the downloaded APK on your device,
4. Tap allow installation of apps from unknown sources (you will want to set this option anyway to be able to install apps built on your device in Termux),
5. Allow the installation to complete,
Once installed, you will see the Termux launcher on your home screen and in your App Drawer. Tap the icon to fire up the application.

#### Installion of termux addon
So if you install termux app from playstore then install addon from playstore as well, if you install termux from fdroid then install addon from fdroid.just simple.
#### why you should not mix sources ?
Here I mean that if you install termux application from playstore then make sure addons like termux api, termux boot etc should installed from playstore, if you try to install from fdroid you won't be succeed. 

Since termux:boot and few more addons are not free on playstore, so people want to install that addon from another free version, so in this case you can't get success.

in short, termux and it's addon are shared user application that's why termux can access it's addon data without root.
here android policy is that , shared user application must have same signature,and you know that different app store use different keystore and signature.








