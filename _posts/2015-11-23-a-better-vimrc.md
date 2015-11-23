---
layout: post
title: a better vimrc
categories:
date: 2015-11-23 10:50:07
---

## Using vim's internal file explorer

I've seen this on [this](https://medium.com/@mozhuuuuu/vimmers-you-dont-need-nerdtree-18f627b561c3) blogpost while looking up some proper keybindings for the NERDtree plugin.  
Since I really don't need anything more than just a simple filebrowser that can be toggled into view, this fits all my needs.  

+  activate the Explorer by type :E in command mode  
+  type "i" for changing list style or just put *let g:netrw_liststyle=3* in your .vimrc  
+  hitting enter on a file will open it in a new buffer (nerdtree seems to open files in new tabs)  
+  if you just want to leave the explorer view, simply go to the next buffer  
+  I've mapped *:E* to *\<ctrl-e\>* in my .vimrc, although that is only slightly, if at all, more convenient 
