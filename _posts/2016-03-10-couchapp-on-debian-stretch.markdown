---
layout: post
title: Couchapp on Debian Stretch
date: 2016-03-10 14:17:00 +0800
type: post
categories: couchdb
---
I have been developing application using [Qooxdoo](http://qooxdoo.org) for years.
It works great so far, except when the internet very slow, which is quite common problem.
It make the application behave unexpectedly weird because user will randomly click
anywhere while data loading from the server.

One way to solve this problem is to design using offline first concept. 
That is where i get to know about [PouchDB](http://pouchdb.com) and  [CouchDB](http://couchdb.apache.org).
[Couchapp](https://github.com/couchapp/couchapp) is a convinient way to develop application on CouchDB.

Installing couchapp is pretty easy,

    #aptitude install python-pip
    #pip install couchapp


Then creating a new project,

    $couchapp generate hello



Related  
[Couchapp on github](https://github.com/couchapp/couchapp)  
[Couchapp documentation](http://docs.couchdb.org/en/latest/couchapp/ddocs.html)  
[Building couchapp](http://www.ibm.com/developerworks/opensource/tutorials/os-couchapp/index.html)



