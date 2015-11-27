---
layout: post
title: mediawiki
categories:
date: 2015-11-27 08:29:25 +0100
---

## Anpassungen, um das Panel beutzbar zu machen

Der "Sidebar" inkl. Logo und allem heißt im html "mw-panel". Mit position:fixed bekommt man den fixiert.  
Entweder in Mediawiki:Common.css oder direkt irgendwo in /mediawiki/ reinschreiben (wo?)  
Der generierte toc_holder müsste im Portal erscheinen, der entsprechende div heißt '#p-', class 'portal'. toc braucht dann entsprechend nicht mehr 'fixed' zu sein  

