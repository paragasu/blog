---
layout: post
title: Set ux31e LCD brightness to the minimum
date: 2014-06-08 08:53:44.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags:
- ux31e
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
  geo_public: '0'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
Add the following line to the _/etc/rc.local_.  

    echo 0 > /sys/class/backlight/acpi_video0/brightness  

