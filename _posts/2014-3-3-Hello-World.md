---
layout: post
title: first glance at working with git
categories:
date:   2014-05-02 10:52:39
---

To get the complete "directory" i.e. repository for https://github.com/gestos/gestos.github.io to my local machine I'd just take the "clone url" that sits on the right hand side of the repository and execute [code]git clone https://github.com/gestos/gestos.github.io.git[/code].

This will create a directory (=repository, since it's a clone of the one at github) called gestos.github.io on the local machine.
Afaic there's no _site directory under in this repository, I guess that's because the actual serving of the site takes place on github and <b>only</b> the "source code" of the site will be in the repository.
I decided to keep it that way and have my site built to an extra dir with the -d option. So, assuming I'm in my local repository, [code]jekyll build -d /path/to/site/root/[code] will put the actual html for the webserver in a different directory than where we're fiddling with the settings. Nice :-).
At this point and because I never had to look into git, this one here http://rogerdudler.github.io/git-guide/ made a nice first aid.
So, after commiting changes in my local repository I can push the stuff up to the "cloud" at github with git push origin master. This would, I guess, translate to: push TO THE origin (meaning github, I think) THIS master BRANCH (i.e. the directory I'm in or so).
Ah; there's a hidden dir called .git in this repository, in which there resides e.g. a file called config that has some info about what is origin and master. I need to figure that out some more - for now it's ok to see that the above command works.
just another jchange
