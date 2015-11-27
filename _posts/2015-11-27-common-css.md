---
layout: post
title: common.css
categories:
date: 2015-11-27 09:52:37 +0100
---

~~~
/* CSS placed here will be applied to all skins */

/* this will keep the panel fixed; watch out for the panels content not to exceed standard height */
#mw-panel {
position: fixed;
}

.tocholder {
line-height: 1em;
padding: 0px 0px;
margin: 0px;
overflow: hidden;
font-size: 0.85em;
position: fixed;
max-height: 70%;
max-width: 200px;
overflow-y: auto;
direction: rtl;
/* left: 0; */
/* top: 0; */
}

#toc, .toc, .mw-warning {
    border: 0px solid #AAA;
    background-color: #F9F9F9;
    padding: 1px;
    font-size: 75%;
    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAAAAAA6fptVAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAApJREFUCB1j+AYAAPgA9yk7T4wAAAAASUVORK5CYII=");
}

.tochidden {
    width: 160px;
}

#p-navigation {
padding-top: 2em;
}

div#mw-panel { 
width: 12em;
position: fixed;
 }
~~~
