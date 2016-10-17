---
layout: post
title: Installing CouchDB 2.0 on Debian Stretch
date: 2016-10-17 09:08:00 +08:00
type: post 
---

CouchDB 2.0 released on September 2016 has clustering support.

    #cd /usr/src
    #wget http://www-eu.apache.org/dist/couchdb/source/2.0.0/apache-couchdb-2.0.0.tar.gz
    #tar xvzf apache-couchdb-2.0.0.tar.gz
    #cd apache-couchdb-2.0.0
    #./configure
    #make release

By any chance you encounter this error,

    ERROR: Unable to generate spec: read file info /usr/lib/erlang/man/man1/gcc-ar.1.gz failed 
    ERROR: Unexpected error: rebar_abort   
    generate failed while processing  rebar_abort 

You need to install erlang-base-hipe instead of erlang-base

    #aptitude install erlang-base-hipe
    #rm /usr/lib/erlang/main
    #make clean
    #make release
