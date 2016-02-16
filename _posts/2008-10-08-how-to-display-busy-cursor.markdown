---
layout: post
title: How to display busy cursor
date: 2008-10-08 05:24:06.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- application
- gtk
- set displayed cursor
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
Interesting post on gtk-app-devel-list@gnome.org mailing list

    void busy_stuff ()
    {
      GdkDisplay *display;
      GdkCursor *cursor;
      GdkWindow *window;
      gint x, y;

      cursor = gdk_cursor_new(GDK_WATCH);
      display = gdk_display_get_default();
      window = gdk_display_get_window_at_pointer(disp, &amp;x, &amp;y);
			gdk_window_set_cursor(window, cursor);
      gdk_display_sync(display);
      gdk_cursor_unref(cursor);

      /* do time-consuming stuff here */
      gdk_window_set_cursor(window, NULL);

    }

gdk_cursor_unref() prevent memory leak

More on [Mailing list archive](http://mail.gnome.org/archives/gtk-devel-list)
