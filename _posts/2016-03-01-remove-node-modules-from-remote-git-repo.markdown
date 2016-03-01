---
layout: post
title: Remove node_modules from remote git repo
date: 2016-03-01 15:32:00 +0800
categories: git
---
node_modules folder in the root project directory can be very large and slow down commit.  
This command will overwrite history.

  
    $git filter-branch -f --tree-filter 'rm -rf node_modules' HEAD 
    $git gc --prune
    $git push origin master --force



Related  
[Permanently remove files and folders from Git repo](http://dalibornasevic.com/posts/2-permanently-remove-files-and-folders-from-a-git-repository)


