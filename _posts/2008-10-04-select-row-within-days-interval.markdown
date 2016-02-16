---
layout: post
title: Select row within days interval
date: 2008-10-04 00:54:01.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags:
- day
- interval
- select
- sql
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
---

    SELECT * FROM mytable WHERE mydate > DATE_SUB(now(),INTERVAL 7 DAYS)
