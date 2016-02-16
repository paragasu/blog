---
layout: post
title: "[Genymotion] [Fatal] Cannot mix incompatible Qt library (version 0x40806)
  with this library (version 0x40802)"
date: 2015-06-05 02:25:35.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags:
- debian
- genymotion
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '11350413814'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---

Go into genymotion installation directory

    #cd /opt/genymotion
    #aptitude install libxi-dev libxmu-dev
    #mkdir QtLibs
    #mv *Qt*.so* QtLibs

Related  
[Ubuntu Forums](http://ubuntuforums.org/showthread.php?t=2207219&amp;p=13048000#post13048000)
