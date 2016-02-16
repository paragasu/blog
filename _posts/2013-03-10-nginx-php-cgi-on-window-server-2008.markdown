---
layout: post
title: nginx + php-cgi on window server 2008
date: 2013-03-10 13:19:54.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
- php
tags:
- nginx window
- php-cgi window
- window server 2008
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

php-cgi.php just hang and die on a very low load.
To fix this, use [spawn-php](https://bitbucket.org/cybergene/spawn-php/wiki/Home)  

Install

    ActivePython-2.7.2.5-win64-x64.msi
    pywin32-217.win-amd64-py2.7.exe

Change nginx configuration
worker_processes  1;

    events {
      worker_connections  1024;
    }

    http {
      include       mime.types;
      default_type  application/octet-stream;
      sendfile        on;
      keepalive_timeout  65;

      upstream php_farm {
       server 127.0.0.1:9000 weight=1;
       server 127.0.0.1:9001 weight=1;
       server 127.0.0.1:9002 weight=1;
       server 127.0.0.1:9003 weight=1;
       server 127.0.0.1:9004 weight=1;
       server 127.0.0.1:9005 weight=1;
       server 127.0.0.1:9006 weight=1;
       server 127.0.0.1:9007 weight=1;
       server 127.0.0.1:9008 weight=1;
       server 127.0.0.1:9009 weight=1;
      }


    server {
      listen       80;
      server_name  localhost;
      location / {
       root   html;
       index  index.php index.html index.htm;
      }

      error_page   500 502 503 504  /50x.html;
       location = /50x.html {
       root   html;
      }
 
      location ~ \.php$ {
       root           html;
       fastcgi_pass   php_farm;
       fastcgi_index  index.php;
       fastcgi_param  SCRIPT_FILENAME  c:/nginx/html/$fastcgi_script_name;
       include        fastcgi_params;
      }
    }

