---
layout: post
title: MSSQL last insert id
date: 2013-02-17 18:40:51.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags: []
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---

Using SCOPE_IDENTITY(),

    $result = sqlsrv_query($conn, 'INSERT INTO mytable(name) values ('hello world') ; 
                                   SELECT SCOPE_IDENTITY() AS ID', array(), $option);
    sqlsrv_next_result();

    $row = sqlsrv_fetch_object($result);
    echo $row->ID; //last insert id


