---
layout: post
title: Cloning object in qooxdoo
date: 2012-09-03 14:35:11.000000000 +08:00
type: post
published: true
status: publish
categories:
- javascript
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

Object

    var a = {};
    var b = qx.lang.Object.clone(a);

Array

    var a = [];
    var b = a.slice();


