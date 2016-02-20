---
layout: post
title: Centos 6 No package php-fpm available
date: 2015-05-27 07:06:06.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags:
- Linux
- php
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '11053383853'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

After installing epel and remi repository and enable remi-php56, the php packages still not available.   
The issue is i just uninstall Cpanel from my Centos 6 server. Cpanel disable php packages from showing up in you.

    #vim /etc/yum.conf


    [main]
    exclude=php* ..


Just remove php packages from the exclude section of the _/etc/yum.conf_.  
It waste 3 hours of my time to figure this out.. :(


