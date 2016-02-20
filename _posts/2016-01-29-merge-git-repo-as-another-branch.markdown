---
layout: post
title: "Merge git repo as another branch"
date: 2016-01-29 16:53:00 +0800 
categories: git
---

I have two local repository on my directory api-php and api-nodejs.
I want to have one repo called api with two branch php and nodejs. 

    $cd api-php
    $git remote add nodejs ../api-nodejs
    $git remote update
    $git checkout -b nodejs
    $git rm -f *
    $git merge nodejs/master 
    $git push -f


By the way, both php and node js implement the same api but the language is totally differnet.  
It is best to put both project on separate repository.


Related  
[Merge git repo into branch of another repo](http://stackoverflow.com/questions/21353656/merge-git-repo-into-branch-of-another-repo)
