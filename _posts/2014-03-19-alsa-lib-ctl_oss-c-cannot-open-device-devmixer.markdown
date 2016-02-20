---
layout: post
title: ALSA lib ctl_oss.c Cannot open device /dev/mixer
date: 2014-03-19 08:31:30.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags: []
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
It happen recently on my debian workstation

    ALSA lib ctl_oss.c:398 (_snd_ctl_oss_open) Cannot open device /dev/mixer
    Cannot open mixer: No such file or directory

When you try to run alsamixer. The reason is the the module snd-pcm-oss not loaded. To fix

    #modprobe snd-pcm-oss
