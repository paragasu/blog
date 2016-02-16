---
layout: post
title: Migrating from MySQL to PostgreSQL
date: 2015-10-29 02:50:01.000000000 +08:00
type: post
published: true
status: publish
categories:
- database
- postgresql
tags:
- migrating
- mysql
- postgresql
meta:
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
  _publicize_job_id: '16314371518'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---
Encounter some issue along the way    

1.MySQL DATE_SUB &amp; DATE_ADD  

    (DATE_ADD(NOW(), INTERVAL 30 MINUTES)
    (DATE_SUB(NOW(), INTERVAL 30 MINUTES)
    (NOW() - INTERVAL '30' MINUTE)
    (NOW() - INTERVAL '30' MINUTE) or
    (NOW() - INTERVAL '30 MINUTES') or
    (NOW() - '30 MINUTES'::INTERVAL)

2.MySQL RADIANS  
Need to cast to real

    SELECT RADIANS(lat::real);

3.DISTINCT on json field (v9.4.5)

    SELECT DISTINCT id, json_field FROM driver;

Throw could not identify an equality operator for type json error.  
Converting the json field to jsonb solve the problem


