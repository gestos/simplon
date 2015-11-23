---
layout: post
title: customizing, pt. 1
categories:
date:   2015-05-02 10:52:39
---

OK, so I'm trying to figure out how Jekyll and its components work, **very** slowly, step by step.

I want to make some changes to the base layout that this fork came with, and there are several considerations:
a) I'd like to use git to be able to go back to the original layout, in case I mess up my customization. Maybe it's possible to clone/fork/branch the repository and keep the current state somewhere archived? -> needs some reading about git
b) from what I see so far, the default layout refers to a style.css file in the sites basedirectory. Obviously its not the source-directory, but the dir to where the site is actually built. In the base-source-directory, there's a file called style.scss. From what I know, scss (or/and sass (?)) are preprocessors.
So most probably style.scss has the parameters that, on building the site, get translated into a "real", final style.css file, that's use on the actual finished site. Let's see what the style.scss contains and how to modify that.
Also let's see what page.html and post.html in the _layouts directory contain and to which .css they point, if any. 

For this Layout:
There is a file _sass/_variables.scss which contains variables that can be used in the style.scss file. E.g. I put into the variables file some colors like *$gestos_skyblue: #A7CDEF;* and into the style.scss I write *background: $gestos_skyblue;*, then on rebuilding the site, the background will be *#A7CDEF*;



-just another little trick for switching panes in vim (like from Nerdtree oder the help pane to an open pane) like shown here: http://stackoverflow.com/questions/1656591/how-to-jump-back-to-nerdtree-from-file-in-tab 
Works in command mode.
