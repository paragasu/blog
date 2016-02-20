---
layout: post
title: Sqlsrv driver return datetime colum as datetime object
date: 2013-02-17 02:33:23.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
tags: []
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
  _wp_old_slug: sqlsrv-driver-return-datetime-colum-as-datetime-object
author:
  login: paragasu
  email: paragasu@gmail.com
---

MSSQL's PHP driver sqlsrv_fetch_object return DateTime object by default.   
To disable this, pass parameter ReturnDatesAsString on the connection string.


    $param = array('Database' => 'db',
                   'UID' => 'uname',
                   'PWD' => 'secret',
                   'ReturnDatesAsStrings' => 'true');

    $conn = sqlsrv_connect('localhost\sqlexpress', $param);



