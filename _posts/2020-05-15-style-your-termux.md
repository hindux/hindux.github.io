---
layout: post
comment: true
title: "Setup termux-styling and change your termux looks"
description: "setup termux-styling ,give unique looks of your terminal , setup termux-styling for free and change font and color with script"
author: kcubeterm
category: termux
tags: [termux,style,]
image: https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/style.jpg
---
There are two methods of styling termux,
* Install termux-styling apps
* By simple hacks.

#### Install termux-styling
So installing application from playstore is't rocket science i guess.


But here's an important point ,if you have installed termux application from another source other than playstore then you cant install apps from google playstore.

Termux and its addon should be install from same source otherwise you cant use it.
I want to tell you that it's not fault or intentions of termux developers, its a restrictions of android 

#### Install it for free
Now we know that termux styling is't a free applications, But in reality, its free
. Termux is an open source project that's why we should donate, you can donate by purchasing apps from playstore
or by [Donate in Termux projects](https://termux.com/donate.html)

For installing application for free, Termux developer uploads termux app and its addon on two platfrom first is google playstore and second is fdroid


**Here i want to suggest that install termux app from trusted source like fdroid and google playstore.**

Now uninstall all termux and its addon from your android.in order to  prevent from mess up of different sources
and go to fdroid and download termux and all addons if you want.
[ link of all fdroid](https://search.f-droid.org/?q=Termux&lang=en) must download latest version.

##### color your terminal
After installing all things , just follows some more steps:


Open Termux application and after that long press

Now it will show you three options "copy paste more"
click on more, and then click on style and then it will show you choose font and choose colour.
 choose whatever you want


#### Termux styling without installing any apps.
In short, you have to write two files one for changing font and another one for changing colors.

Now change your directory 
```
cd ~/.termux
```
For changing color you have to write `colors.properties` and for font you have to write `font.ttf`

Termux has already some themes and fonts in sources , so we just download from there.
theme [link](https://github.com/termux/termux-styling/tree/master/app/src/main/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/colors)
fonts [link](https://github.com/termux/termux-styling/tree/master/app/src/main/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/fonts)

change current theme into another
```
curl -o colors.properties https://raw.githubusercontent.com/termux/termux-styling/master/app/src/main/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/colors/base16-apathy-light.properties
termux-reload-settings

```
here you can download any themes from above link

Now change font
```
curl -o font.ttf https://raw.githubusercontent.com/termux/termux-styling/master/app/src/main/https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/fonts/Go.ttf

termux-reload-settings
```

if you face any issue with it,comment or report issue on https://github.com/Hindux/hindux.github.io/issues

