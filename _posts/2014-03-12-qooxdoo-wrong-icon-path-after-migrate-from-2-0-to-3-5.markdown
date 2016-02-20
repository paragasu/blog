---
layout: post
title: Qooxdoo wrong icon path after  migrate from 2.0 to 3.5
date: 2014-03-12 12:58:37.000000000 +08:00
type: post
published: true
status: publish
categories:
- Qooxdoo
tags: []
meta:
  _publicize_pending: '1'
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

It must be in the form below, start by "/**" and end by "*/" and in between start by "*".

    /**
    * @assert(sumisi/*)
    */

Otherwise assert will not be read by JsDoc and give an error.

    qx.ui.basic.Image[90-0]: Image could not be loaded: sumisi/login.png
    ImageLoader: Not recognized format of external image 'sumisi/login.png'


