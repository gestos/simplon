---
layout: post
title: apache process spawning
categories:
---

Having had apache running for some hours, I came to notice that there were 5 or more processes, each having several thread, I wondered why this heavy spawning of processes occured. There are several files that can influence apaches behaviour, namely: apache2.conf - keepalive (on|off) and in the mods directory mpm_event.conf, mpm_prefork.conf and mpm_worker.conf. Depends on whether the apache is running as prefork or worker module, I guess. You can set MaxSpareServers and the like to lower values, and apache won't spawn as many child processes. I know nothing about the exact behaviour, especially regarding the keepalive option.
