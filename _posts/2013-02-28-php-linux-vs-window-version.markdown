---
layout: post
title: PHP linux vs window version
date: 2013-02-28 16:45:53.000000000 +08:00
type: post
published: true
status: publish
categories:
- php
tags:
- php window vs linux
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
Come across interesting fact:
In linux

    echo $_SERVER['SERVER_NAME']; //somedomain.org
    echo $_SERVER['HTTP_HOST']; //somedomain.org

In window  

    echo $_SERVER['SERVER_NAME']; //localhost
    echo $_SERVER['HTTP_HOST']; //somedomain.org


