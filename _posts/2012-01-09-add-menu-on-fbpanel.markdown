---
layout: post
title: Add menu on fbpanel
date: 2012-01-09 00:28:25.000000000 +08:00
type: post
published: true
status: publish
categories:
- Linux
tags: []
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

If you install binary manually eg: eclipse. Most likely you end up without entries in FBpanel the start menu.
Just create a file appname.desktop in then ~/.local/share/applications

    [Desktop Entry]
    Type=Application
    Name=Eclipse
    Exec=/opt/eclipse/eclipse
    Icon=/opt/eclipse/icon.xpm
    NoDisplay=false
    Categories=Development
