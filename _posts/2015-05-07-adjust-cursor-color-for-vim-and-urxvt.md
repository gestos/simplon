---
layout: post
title: adjust cursor color for vim and urxvt
categories:
date: 2015-05-07 19:39:59
---

Whenever I used a dark colour scheme for vim (like the excellent <a href="https://github.com/gregsexton/Muon">muon</a> or <a href="https://github.com/larssmit/vim-getafe/tree/master/colors">getafe</a>), I found myself lost beacuse the usually black cursor of my urxvt wouldnt adjust to the dark colour theme. I found that this cant be tweaked in vim, but one can change the color of the urxvt terminal; so, for my needs, 
URxvt*cursorColor:  #D6C0FB
URxvt*cursorBlink:  on
does the job pretty satisfyingly :-)
(for reloading the Xresources, use xrdb -load .Xresources. put the same command into ~/.xinitrc to have it loaded on X startup)
