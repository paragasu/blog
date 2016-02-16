---
layout: post
title: Using g_value_get_*
date: 2008-10-04 00:39:28.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- GValue
- g_value_get_float
- g_value_get_int
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
Using GValue related function is quite tricky. It is not working if you do

    GdaDataModel *dm;
    gint i;
    i = g_value_get_int ( gda_data_model_get_value_at (dm, 0, 0));


For upcomming Version 4.0 (the main difference is at GdaDataModel API)

    GdaDataModel *model;
    const GValue *integer;
    GError *error = NULL;
    integer = gda_value_new (G_TYPE_INT);
    integer = gda_data_model_get_value_at  (model, 0, 0, &error);


All values in a Data Model must be unmodificable then use const GValue, this will avoid compilation warnings. 
Or can use (gda_value_new makes this for you :-)

    integer = g_new0 (GValue. 1);
    g_value_init (inteteger, G_TYPE_INT);


Thanks to Daniel Espinosa

