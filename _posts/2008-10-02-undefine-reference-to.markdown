---
layout: post
title: Gtk undefine reference
date: 2008-10-02 23:02:02.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- makefile
- static
- undefine reference to
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
---

Header file and function on separate file should not have the static function declaration.

    static void loan_new_record (gpointer data);
    static void loan_display_reset ( GtkWidget *data); 

to

    void loan_new_record (gpointer data);
    void loan_display_reset ( GtkWidget *data);


[Read more](http://www.gtkforums.com/viewtopic.php?t=1830)
