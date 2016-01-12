---
layout: post
title: Qooxdoo change global application font size
date: 2015-06-29 16:13:04.000000000 +08:00
type: post
published: true
status: publish
categories:
- javascript
- Qooxdoo
tags:
- change font size
- qooxdoo
meta:
  _edit_last: '5225680'
  geo_public: '0'
  _publicize_job_id: '12153595090'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

	setFontSize: function(size)
	{
		var doc         = this.getRoot();  
		var manager     = qx.theme.manager.Font.getInstance();  
		var defaultFont = manager.resolve(doc.getFont());
		var newFont     = defaultFont.clone().setSize(parseInt(size));
		doc.setFont(newFont);
	},  


