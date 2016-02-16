---
layout: post
title: save image and display image from postgresql
date: 2008-09-29 06:26:10.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- display image
- gtk
- postgresql
- save image
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
---

There is several way to save image into postgresql database. Using oid, blob and bytea data types.bytea column type recommended.

To store image

    gdk_pixdata_from_pixbuf(),
    gdk_pixdata_serialize()

To display image

    gdk_pixdata_deserialize(),
    gdk_pixbuf_from_pixdata(),
    gtk_image_new_from_pixbuf() 


Thanks to vivien and Yann Droneaud for great help

Related  
[Gdk Pixbuf inline](http://library.gnome.org/devel/gdk-pixbuf/stable/gdk-pixbuf-inline.html)  
[Libgnomedb example](http://svn.gnome.org/viewvc/libgnomedb/trunk/libgnomedb/plugins/common-pict.c?revision=1686&amp;view=markup)

