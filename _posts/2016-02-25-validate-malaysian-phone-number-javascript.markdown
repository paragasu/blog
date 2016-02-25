---
layout: post
title: Validate malaysian phone number in javascript
date: 2016-02-25 09:52:00 +0800
type: post
categories: javascript
---
My pull request just accepted by chriso author of validator.js, now you can use validator.js 
to validate malaysian phone number using 'ms-MY' locale.  

Probably will take sometime before the npm and bower package updated.  
You can install via npm,

    $npm install --save https://github.com/chriso/validator.js.git

On nodejs, 

    const v = require('validator')
    v.isMobilePhone('+60128747889', 'ms-MY')

On browser,

    <script type="text/javascript" src="validator.min.js"></script>
    <script type="text/javascript">
      validator.isMobilePhone('+60128747889', 'ms-MY') //true
    </script> 



Btw, i wish the locale is en-MY but there is no such thing. So, i think ms-MY will do.


Related  
[Telephone number in malaysia](https://en.wikipedia.org/wiki/Telephone_numbers_in_Malaysia)  
[Github validator.js](https://github.com/chriso/validator.js)
