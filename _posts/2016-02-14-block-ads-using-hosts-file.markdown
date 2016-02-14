---
layout: post
title: "Block ads using /etc/hosts in debian"
date: 2016-02-14 23:57:00 +0800  
categories: linux
---
We can avoid ads from loading by serving 0.0.0.0 or 127.0.0.1 for the ads domain.   
There is a few website that provide such list and one of them is from mvps.org.  

The installation is rather simple. Just copy and paste the list to /etc/hosts file.

    #wget http://winhelp2002.mvps.org/hosts.txt
    #cp /etc/hosts /etc/hosts.old
    #cat hosts.txt >> /etc/hosts

The host file come from window enviroment. So there will be some extra line ugly line   
ending that look like ^M in vim. To fix it

    #vim /etc/hosts

Then on the vim command mode run  

    :%s/<CTRL-V><CTRL-M>//g



Related  
[Block unwanted advertisements with /etc/hosts file on Linux ](http://www.putorius.net/2012/01/block-unwanted-advertisements-on.html)  
[Amalgamated hosts file](https://github.com/StevenBlack/hosts)


