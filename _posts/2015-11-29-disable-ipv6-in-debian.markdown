---
layout: post
title: Disable ipv6 in debian
date: 2015-11-29 09:46:43.000000000 +08:00
type: post
published: true
status: publish
categories: linux
tags:
- debian
- ipv6
- Linux
---

Edit /etc/sysctl.conf and add config

	net.ipv6.conf.all.disable_ipv6 = 1
	net.ipv6.conf.default.disable_ipv6 = 1
	net.ipv6.conf.lo.disable_ipv6 = 1
	net.ipv6.conf.eth0.disable_ipv6 = 1

	#sysctl -p


[Debian IPV6](https://wiki.debian.org/DebianIPV6)
