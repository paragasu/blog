---
layout: post
title: "Install gin.io in debian jessie"
date: 2016-01-27 17:34:00 +0800  
categories: openresty
---
Openresty is nginx with embeded lua
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
[Gin Json Api framework](http://gin.io)



