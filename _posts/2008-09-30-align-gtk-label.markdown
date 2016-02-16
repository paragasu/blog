---
layout: post
title: Align gtk label using gtk_misc_set_alignment()
date: 2008-09-30 04:32:46.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- alignment
- gtk
- gtk_misc_set_alignment
- justify
- label
- table
- tutorial
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
When packing a gtk label inside gtk table. I come across one problem. All the label as aligned center.   
As a result i just made one ugly form. To fix the problem, use gtk_misc_set_alignment().  

![Gtk screenshot](/assets/tablescr.png "gtk label with gtk_misc_set_" width="208" height="128")

See code example

    #include <gtk/gtk.h>
    int main (int argc, char **argv)
    {
      GtkWidget *window;
      gtk_init( &amp;argc, &amp;argv);
      window = gtk_window_new(GTK_WINDOW_TOPLEVEL);
      GtkWidget *table = gtk_table_new( 4, 1, TRUE );
      GtkWidget *label;
      label = gtk_label_new("Normal label");
      gtk_table_attach_defaults ( GTK_TABLE(table), label, 0, 1, 0, 1)
      label = gtk_label_new( "left" );
      gtk_misc_set_alignment( GTK_MISC(label), 0.0, 0.0 );
      gtk_table_attach( GTK_TABLE(table), label, 0, 1, 1, 2,
                        GTK_EXPAND|GTK_FILL, GTK_SHRINK, 0, 0 ); /*important*/
      label = gtk_label_new( "center" );
      gtk_misc_set_alignment( GTK_MISC(label), 0.5, 0.0 );
      gtk_table_attach_defaults( GTK_TABLE(table), label, 0, 1, 2, 3
                                 GTK_EXPAND|GTK_FILL, GTK_SHRINK, 0, 0 ); /*important*/
      label = gtk_label_new( "right" );
      gtk_misc_set_alignment( GTK_MISC(label), 1.0, 0.0 );
      gtk_table_attach_defaults( GTK_TABLE(table), label, 0, 1, 3, 4
                                 GTK_EXPAND|GTK_FILL, GTK_SHRINK, 0, 0 ); /*important*/
      gtk_widget_set_size_request (GTK_WIDGET (table), 200, 100);
      gtk_container_add( GTK_CONTAINER (window), GTK_WIDGET(table));
      gtk_widget_show_all(window);
      gtk_main();
      return 0;
    }


Thanks to [owl102](http://www.gtkforums.com/viewtopic.php?t=1792) from gtkforums.com
