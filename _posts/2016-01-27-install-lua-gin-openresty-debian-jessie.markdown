---
layout: post
title: "Install gin.io in Debian Jessie"
date: 2016-01-27 17:34:00 +0800  
categories: openresty
---
Openresty is nginx with embeded lua. High performance with low memory footprint.      
Gin is a small and elegant lua framework build on top of Openresty.

Install Openresty framework


    #aptitude install lua-dbi-postgresql-dev  
    #aptitude install luajit  
    #aptitude install libreadline-dev libncurses5-dev libpcre3-dev libssl-dev perl make build-essential
    #aptitude install libpq-dev
    #cd /usr/src
    #wget https://openresty.org/download/ngx_openresty-1.9.7.2.tar.gz
    #cd ngx_openresty*
    #./configure --with-luajit --with-http_postgres_module



Install gin framework  

    #aptitude install luarocks  
    #luarocks install --server=http://gin.io/repo gin  


Related  
[OpenResty](http://openresty.org/)  
[Gin JSON API framework](http://gin.io)



