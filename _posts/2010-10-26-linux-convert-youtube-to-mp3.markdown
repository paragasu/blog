---
layout: post
title: linux convert youtube to mp3
date: 2010-10-26 00:42:21.000000000 +08:00
type: post
published: true
status: publish
categories:
- Open Source
tags:
- conver youtube to mp3
meta:
  _edit_last: '5225680'
  _wp_old_slug: ''
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
    #aptitude install youtube-dl ffmpeg libmp3lame

a simple bash script called youtube

    #!/bin/bash
    x=/tmp/youtube-dl-$RANDOM-$RANDOM.flv
    youtube-dl --output=$x --format=18 "http://www.youtube.com/watch?v=$1"
    echo "convert flv to mp3"
    ffmpeg -i $x -acodec libmp3lame -ac 2 -ab 128k -vn -y "/home/paragasu/mp3/youtube/$2"
    rm $x
    echo "done"

The fun begin

    $youtube linkname fileoutput.mp3

Related  
[Youtube to mp3 on ubuntu linux](http://hubpages.com/hub/Youtube-to-MP3-on-Ubuntu-Linux)
