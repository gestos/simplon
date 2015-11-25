---
layout: post
title: grub default boot
categories: linux debian grub
date: 2015-11-25 09:54:27
---

## have grub remember last choice

One of the things I rarely use and need to look up every time, so why not omit google and write it down here ;)  
To make grub remember the last kernel I chose to boot, I need to set

~~~
/etc/default/grub:

GRUB_DEFAULT=saved
GRUB_SAVEDEFAULT=true
~~~

solution from [askubuntu](http://askubuntu.com/questions/148662/how-to-get-grub2-to-remember-last-choice).
