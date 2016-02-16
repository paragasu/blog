---
layout: post
title: Qooxdoo disable tabview page
date: 2012-09-29 04:10:30.000000000 +08:00
type: post
published: true
status: publish
categories:
- javascript
- Qooxdoo
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

Here is a way to disable the tabview page. Turn it grey and unclickable.

    var page = new qx.ui.tabview.Page("page");
    page.set({enabled: false});
