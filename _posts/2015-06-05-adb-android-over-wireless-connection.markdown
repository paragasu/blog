---
layout: post
title: ADB android over wireless connection
date: 2015-06-05 11:34:14.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags:
- adb wireless
- android
- debian
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '11362653725'
author:
  login: paragasu
  email: paragasu@gmail.com
---

Connect using USB.

    $adb tcpip 5555

Disconnect USB.  

Reconnect using wireless connection. You can find out the IP address from wireless config

    $adb connect 192.168.1.3:5555



