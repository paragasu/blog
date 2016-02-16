---
layout: post
title: "Setting up nfs in debian stretch"
date: 2015-11-08 01:57:58.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags:
- debian stretch
- Linux
- nfs
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
On nfs server

    #aptitude install nfs-kernel-server


Edit /etc/exports configuration file

    /home/me/public 192.168.1.2(rw,no_root_squash,subtree_check)<br />

Restart nfs

    #exportfs -a
    #/etc/init.d/nfs-kernel-server start

On nfs client

    #aptitude install nfs-common
    #/etc/init.d/nfs-common start

To list available nfs

    #showmount -e 192.168.1.2

To mount nfs

    #mount -t nfs /home/me/public /mnt/public<br />


Related  
[Basic nfs configuration on debian 7](https://www.linode.com/docs/networking/basic-nfs-configuration-on-debian-7)
