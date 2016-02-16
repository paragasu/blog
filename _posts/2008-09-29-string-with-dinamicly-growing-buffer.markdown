---
layout: post
title: String with dinamicaly growing buffer
date: 2008-09-29 05:12:08.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- c
- overflow
- secure
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
String is where buffer overflow always occur.
GLIB supports doing this much more easily:

    /* portable asprintf() */
    char *str = g_strdup_printf("string%s%d", str_variable, int_variable);


Or if you wanted a modifyable buffer:

    GString *str = g_string_new(NULL);
    g_string_append(str, "string");
    g_string_append(str, str_variable);
    g_string_sprintfa(str, "%d", int_variable); /* no g_string_append_int() */


Related  
[Secure, Efficient and Easy C programming](http://www.irccrew.org/~cras/security/c-guide.html)
