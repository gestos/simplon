---
layout: post
title: freeciv localhost
categories:
date: 2015-12-13 11:11:02 +0100
---

## problems starting local freeciv games
I ran into this several times and spent hours looking for the solution, forgetting it immediately afterwards.  
When the freeciv client can't connect to the local server, although it's up and running and everything in /etc/hosts and resolv.conf seems to be fine:  
the /etc/hosts file comes by default with an ipv6 entry like localhost ::1  
This will make the client search for the server with the ipv6 protocol. In my case, ipv6 is not available, yet the entry is still there.
Out-commenting that line will make things work ;-).
