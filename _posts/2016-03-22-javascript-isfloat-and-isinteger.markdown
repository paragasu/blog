---
layout: post
title: isFloat and isInteger in javascript
date: 2016-03-22 16:45:00 +0800
type: post
categories: javascript
---

Found some interesting way to check isFloat and isInteger in javascript on stackoverflow

    function isFloat(n) {
      return n === +n && n !== (n|0);
    }

    function isInteger(n) {
      return n === +n && n === (n|0);
    }


Related  
[How do i check that a number is a float or integer](http://stackoverflow.com/questions/3885817/how-do-i-check-that-a-number-is-float-or-integer)
