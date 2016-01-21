---
layout: post
title: dhcpcd ohne dns
categories:
date: 2015-12-09 21:40:00 +0100
---

## dhcpcd daran hindern, den Nameserver vom dhcp-Server zu beziehen

Um zu verhindern, daß dhcpcd jedes Mal vom dhcp-Server den dns-server zieht und resolv.conf überschreibt, hilft folgender Eintrag in /etc/dhcpcd.conf:  
<code>nohook resolv.conf</code>
Siehe [archlinux wiki](https://wiki.archlinux.org/index.php/Resolv.conf#Modify_the_dhcpcd_config)
Andere Lösungen sind entweder an die NIC gebunden (siehe [gentoo wiki](https://forums.gentoo.org/viewtopic-p-6183922.html?sid=0bf842f147608b18fdb3d78194fc83dd#6183922)) oder funktionieren einfach nicht (statischer DNS in dhcpcd.conf wie im Arch-wiki beschrieben).
