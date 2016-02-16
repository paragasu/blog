---
layout: post
title: Using Makefile
date: 2008-09-29 03:22:12.000000000 +08:00
type: post
published: true
status: publish
categories:
- gtk
tags:
- c
- gtk
- Linux
- make
- makefile
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---
If you writing gtk application. You will have to use more than one source file to make the code more manage able. To compile the application you need to use make.
![Makefile image](/assets/makefile.jpeg "makefile tutorial")

It is all you need to compile a c code with libgnomedb. This code will output an executable
file with name ekoken. A more complicated makefiles using variable is like this

    CC = gcc
    LD = gcc
    CFLAGS =
    RM = rm -f
    LDFLAGS = `pkg-config --libs gtk+-2.0`
    PROG =
    OBJS =

    all : $(PROG)
    %.o : %.c
    $(CC) $(CFLAGS) -c $&lt; -o $@
    $(PROG) : $(OBJS)
    $(LD) $(LDFLAGS) $(OBJS) -o $(PROG)

    clean :
    $(RM) $(OBJS) $(PROG)


Where PROG is the executable output and OBJS is the object file output with .o suffix.

Related  
[Makefile in C or C++](http://helpdesk.cs.tamu.edu/docs/makeFile)  
[A simple makefile tutorial](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor)
