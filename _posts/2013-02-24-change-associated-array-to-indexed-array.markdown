---
layout: post
title: Change associated array to indexed array
date: 2013-02-24 08:47:59.000000000 +08:00
type: post
published: true
status: publish
categories:
- php
tags:
- array
- php
meta:
  _edit_last: '5225680'
  _publicize_pending: '1'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
  first_name: ''
  last_name: ''
---
Sometimes i want to change this form of array

    array(
      'position' => array('data1', 'data2'..)
      'year'     => array('year1', 'year2'..)
    )

to this


    array(0 => array('position' =>'data1',
                     'year' => 'year1'),

          1 => array('position' => 'data2',
                     'year' => 'year2')


Here is how i do it.

    function array_group($data)
    {
      $result = array();

      foreach($data as $key=>$rows)
         foreach($rows as $i=>$value)
             $result[$i][$key] = $value;
      
       return $result;
    }

