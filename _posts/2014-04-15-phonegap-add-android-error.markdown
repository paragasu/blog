---
layout: post
title: Phonegap add android error
date: 2014-04-15 20:35:29.000000000 +08:00
type: post
published: true
status: publish
categories:
- android
tags: []
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---
On the phonegap 3.4 running to command

    $phonegap add android

Give an error like this


    /bin/node_modules/q/q.js:126
                    throw e;
                          ^

The problem is the android sdk still not configured properly
you need to configure the environment ANDROID_HOME, ANDROID_HOME/tools and ANDROID_HOME/platform-tools
add this in your ~/.bash_profile


    export ANDROID_HOME=$HOME/android-sdk-linux
    export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools


