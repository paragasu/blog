---
layout: post
title: Powerdns unable to find backend willing to host for potential supermaster
date: 2015-05-17 02:36:40.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags:
- powerdns
meta:
  _publicize_pending: '1'
  sharing_disabled: '1'
  _rest_api_published: '1'
  _rest_api_client_id: "-1"
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
I got this error when i setup powerdns superslave in debian using sqlite3 backend.   
The condition to get the superslave working.

- The supermaster must carry a SOA record for the notified domain.
- The supermaster IP must be present in the 'supermaster' table.
- The set of NS records for the domain, as retrieved by the slave from the supermaster,  
 *must include the nameserver* that goes with the IP address in the supermaster table.

A very usefull command to test if the setup is working.
To send the notification to the slave and

    #pdns_control notify mydomain.com

To request for supermasters zone

    #pdns_control retrieve mydomain.com


Related  
[PDNS slave operation](https://doc.powerdns.com/md/authoritative/modes-of-operation/#slave-operation)  


