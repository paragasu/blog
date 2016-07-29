---
layout: post
title: Nodejs gotcha on heroku
date: 2016-05-18 11:47:00 +08:00
type: post
---

Use environment variable process.env.PORT instead of requesting for fixed port.
Heroku will assign random port everytime the application bootup. This lead to some misleading
error like strange Redis too many connection error and error H10.

    app.listen(process.env.PORT || 5000);


Another gotcha when we upgrade the PostgreSQL to the bigger plan, yet another misleading error

    error: no pg_hba.conf entry for host 

The paid plan (standard-0) only accept ssl connection:

    postgres://user:seckrit@pghost:5432/dbname?ssl=true

