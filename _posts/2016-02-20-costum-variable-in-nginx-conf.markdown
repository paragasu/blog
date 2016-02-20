---
layout: post
title: Variable in nginx configuration
date: 2016-02-20 10:59:00 +0800
categories: nginx
---
Found one interesting overlook configuration in nginx.

    server {
      server_name ~^(www\.)?(?<domain>.+)$;

      location / {
        root /sites/$domain;
      }
    }

Some note on the matching pattern modifiers,

    (none) prefix match
    =    match exactly
    ~    case sensetive regex match
    ~*   case insensetive regex match
    ^~   non regular match is prefered


Related  
[Nginx core module configuration](http://nginx.org/en/docs/http/ngx_http_core_module.html#server)  
[Understanding server and location block selection algorithm](https://www.digitalocean.com/community/tutorials/understanding-nginx-server-and-location-block-selection-algorithms)  
