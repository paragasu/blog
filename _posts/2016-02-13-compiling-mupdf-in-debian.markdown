---
layout: post
title: "Compile mupdf in debian"
date: 2016-02-13 10:34:00 +0800  
categories: programming
---

    #aptitude install libgl-dev libxcursor-dev libxrandr-dev libxinerama-dev
    $git clone git@github.com:paragasu/mupdf.git
    $cd mupdf
    $git submodule init
    $git submodule update
    $make
