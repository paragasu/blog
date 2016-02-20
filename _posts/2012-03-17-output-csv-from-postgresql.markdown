---
layout: post
title: Output  csv from postgresql
date: 2012-03-17 03:29:57.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

    psql> COPY (SELECT * FROM tablename) TO '/tmp/filename.csv' WITH CSV HEADER;
