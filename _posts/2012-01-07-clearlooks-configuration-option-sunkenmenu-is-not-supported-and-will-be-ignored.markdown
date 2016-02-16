---
layout: post
title: Clearlooks configuration option "sunkenmenu" is not supported and will be ignored.
date: 2012-01-07 05:26:32.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

    $android
    /usr/share/themes/Taqua/gtk-2.0/gtkrc:55: Clearlooks configuration option "sunkenmenubar" is not supported and will be ignored.
    /usr/share/themes/Taqua/gtk-2.0/gtkrc:56: Clearlooks configuration option "menuitemstyle" is not supported and will be ignored.
    /usr/share/themes/Taqua/gtk-2.0/gtkrc:57: Clearlooks configuration option "listviewitemstyle" is not supported and will be ignored

To fix it, uncomment the sunkenmenubar, menuitemstyle and lastviewitemstyle   
in the /usr/share/themes/Taqua/gtk-2.0/gtkrc

    engine "clearlooks"
    {
      #sunkenmenubar = 0
      #menuitemstyle = 0
      #listviewitemstyle =0
    }
