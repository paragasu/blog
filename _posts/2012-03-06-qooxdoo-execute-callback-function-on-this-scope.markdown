---
layout: post
title: qooxdoo execute callback function on this scope
date: 2012-03-06 02:02:08.000000000 +08:00
type: post
published: true
status: publish
categories:
- Qooxdoo
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---

	rpc.callAsync(qx.lang.Function.bind(this._responseReceived, that));  

Now you can refer this in _responseReceived Functions.
