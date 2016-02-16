---
layout: post
title: "Ghost blog mail configuration using Amazon SES"
date: 2016-02-15 15:16:00 +0800  
categories: nodejs
---

Ghost is a blogging platform written in nodejs.  
Edit the config.js file at the ghost root directory

    mail: {
       from: 'from@email.com',
       transport: 'SMTP',
       options: {
         host: "your-amazon-host",
         port: 465,
         service: "SES",
         auth: {
           user: "your-amazon-user",
           pass: "your-amazon-password"
         }
       }
    }

Amazon SES credential can be generated from amazon control panel.  
From address must be registered and verified as sender.


Related  
[Mail configuration on a self hosted ghost](http://support.ghost.org/mail)
[Mail github source](https://github.com/TryGhost/Ghost/blob/master/core/server/mail/index.js)
