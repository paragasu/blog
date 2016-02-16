---
layout: post
title: Oss4 no sound in iceweasel flash
date: 2012-09-17 01:28:51.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

flashplugin-nonfree only support Alsa. Thus, extra package required to support OSS4

    #aptitude install flashplugin-nonfree-extrasound
    #mkdir /usr/lib/oss/lib
    #cd /usr/lib/oss/lib
    #ln -s /usr/lib/flashplugin-nonfree-extrasound/libflashsupport.so


Restart iceweasel
