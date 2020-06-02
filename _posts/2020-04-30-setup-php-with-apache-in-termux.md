---
layout: post
title: "How to integrate php and apache in linux and termux."
author: kcubeterm
categories: termux
tags: [php,apache]
image: https://cdn.jsdelivr.net/gh/hindux/hindux.github.io/assets/images/php-apache.jpg
description: "How to setup and integrate php with apache and control server with php as backened"
featured: true
hidden: true
rating: 4.5
---
As we know without backend language webserver is nothing, and php as backened language fulfill your all requirements with webserver, then let's go

#### Requirements
Termux provide a separate package for php and Apache in which all requirements install automatically by that package.
the name of that package is **php-apache**  By the way it contains modules which loads by Apache .

```
pkg install php-apache

```
and now copy and following in httpd.conf, as i mention in my old [tutorial]({{ site.baseurl }}/setup-apache-server-in-termux)
after that paste following in httpd.conf in last line.

```
LoadModule php7_module libexec/apache2/libphp7.so
<FilesMatch \.php$> 
   SetHandler application/x-httpd-php
</FilesMatch>
<IfModule dir_module>
    DirectoryIndex index.php
</IfModule>
```

and uncomment mpm prefork module and comment mpm worker modules, these two module may found in line 66 and 67 in httpd.conf.
```
LoadModule mpm_prefork_module libexec/apache2/mod_mpm_prefork.so
# LoadModule mpm_worker_module libexec/apache2/mod_mpm_worker.so
```
now the php has linked with apache server, go to document root, the default custom root of apache is `/data/data/com.termux/files/usr/share/apache2/default-site/htdocs`


if you get any type of error, then fresh install all those things, remove php ,apache . fresh installation resolve issues most of the time.


