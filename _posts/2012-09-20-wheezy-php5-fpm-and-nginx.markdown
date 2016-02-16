---
layout: post
title: Wheezy php5-fpm and nginx
date: 2012-09-20 14:55:32.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
- php
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

Debian wheezy version of php5-fpm (5.4.4-7) using socket instead of server running on local port 9000.
Need to update nginx configuration files to point to php5-fpm socket.

    location ~.\.php$ {
      #fastcgi_pass 127.0.0.1:9000;
      fastcgi_pass unix:/var/run/php5-fpm.sock;
    }
