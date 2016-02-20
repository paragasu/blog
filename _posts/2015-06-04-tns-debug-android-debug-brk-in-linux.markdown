---
layout: post
title: tns debug android --debug-brk in linux
date: 2015-06-04 11:10:26.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags:
- chrome
- debug-brk
- google chrome
- nativescript
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '11327250927'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
The nativescript cli

    $tns debug android --debug-brk

The command expect your google chrome executable name is "chrome".  
But in my debian jessie workstation. The executable name is "google-chrome"

    $ln -s /usr/bin/google-chrome ~/bin/chrome

will fix the problem.


