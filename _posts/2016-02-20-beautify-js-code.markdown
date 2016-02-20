---
layout: post
title: Beautify javascript code
date: 2016-02-20 11:30:00 +0800
categories: js
---
Some of my javascript code indent contain mixed of tab and space  
and only aware of the code ugly indent when i open in github.

There is a few cli program to format code and my favorite so far is _js-beautify_

    #npm install -g js-beautify

Go to the source code do

    $js-beautify -h
    $js-beautify -s 2 -r *js

You can make vim to display space character on the editor by using the command

    :set list


