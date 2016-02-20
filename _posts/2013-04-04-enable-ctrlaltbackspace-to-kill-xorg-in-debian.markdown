---
layout: post
title: Enable ctrl+alt+backspace to kill xorg in debian
date: 2013-04-04 16:07:13.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags:
- debian
- Linux
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

Add this into ~/.bash_profile

    setxkbmap -option terminate:ctrl_alt_bksp


