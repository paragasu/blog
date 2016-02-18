---
layout: post
title: Install php7.0 on debian jessie
date: 2016-02-18 20:41:00 +0800
categories: debian
---
The latest PHP7.0 come with huge speed improvement.
PHP7.0 debian package is available from dotdeb repository.

    deb http://packages.dotdeb.org jessie all
    deb-src http://packages.dotdeb.org jessie all

Then install the key

    #wget https://www.dotdeb.org/dotdeb.gpg
    #sudo apt-key add dotdeb.gpg
    #aptitude install php7.0-fpm php7.0-pgsql php7.0-cli

Please note that some extension not yet available.


Related  
[PHP 7.0.3 for jessie](https://www.dotdeb.org/2016/02/06/php-7-0-3-for-jessie)  
[Dotdeb install instruction](https://www.dotdeb.org/instructions)
