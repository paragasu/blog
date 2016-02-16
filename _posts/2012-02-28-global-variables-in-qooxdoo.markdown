---
layout: post
title: Global variables in qooxdoo
date: 2012-02-28 23:50:00.000000000 +08:00
type: post
published: true
status: publish
categories: []
tags:
- qooxdoo
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

Declare the variables in your Application class:

    qx.Class.define("custom.Application",
    {
      extend  : qx.application.Standalone,
      members :
      {
      /** My global variable */
       bGlobal : true
       main : function()
       {
      // access to global variable from within this class using "this"
         this.bGlobal = false;
       }
      }
    }

Then you can access that main application class using *qx.core.Init.getApplication()* so in some other class, you can read  the global like this:

    qx.Class.define("custom.SomeArbitraryClass",
    {
      extend  : qx.core.Object,
      construct : function()
      {
        /** Access the global variable */
        if(qx.core.Init.getApplication().bGlobal)
        {
          alert("The global is TRUE");
        }
      }
    }

You could also have made that global be a property of the Application class:

    qx.Class.define("custom.Application",
    {
      extend  : qx.application.Standalone,
      properties :
      {
      /** My global variable */
       global : true
       ...

In which case you'd reference it from the other class using the property's getter:

    qx.core.Init.getApplicaiton().getGlobal()

