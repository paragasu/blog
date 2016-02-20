---
layout: post
title: How to use genymotion emulator
date: 2015-06-05 11:36:59.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags: []
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '11362717338'
author:
  login: paragasu
  email: paragasu@gmail.com
---

Start the emulator. Then find out the genymotion assigned IP address

    $ps ax | grep geny

Then connect using adb

    $adb connect 192.168.1.3

