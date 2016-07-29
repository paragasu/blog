---
layout: post
title: Debugging and logging in OpenResty
date: 2016-07-29 08:43:00 +08:00
type: post
---

There is a few key point to ease the development of lua in OpenResty environment.

1. Turn lua code caching off

Restarting nginx everytime there is a code changes is painful. 
The easier way is to load external lua code using *content_by_lua_file* as opposed
to have lua code inside nginx configuration files and then turn off the cache.

```
location /hello {
  default_type text/html;
  lua_code_cache off; #development
  content_by_lua ./hello.lua;
}
```

2. Read nginx log as it is written

Set the error_log configuration directive to output log on easily accessable directory.

    error_log /home/away/tmp/hello.log

And read the log interactively in a separate terminal as it been written using

    tail -f /home/away/temp/hello.log


3. Output the log file in the terminal
Redirect all error log to the terminal where nginx is running

    error_log /dev/stderr;


4. Log event or variable
Output debugging info using ngx.log

    ngx.log(ngx.ERR, "hello world here")




References 
[OpenResty website](http://openresty.org) 
[Definintely an OpenResty Guide](http://www.staticshin.com/programming/definitely-an-open-resty-guide)
