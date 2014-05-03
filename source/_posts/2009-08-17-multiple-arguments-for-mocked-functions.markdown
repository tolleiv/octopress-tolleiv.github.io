---
author: tolleiv
comments: true
date: 2009-08-17 21:38:45+00:00
layout: post
slug: multiple-arguments-for-mocked-functions
title: multiple arguments for mocked functions....
wordpress_id: 221
categories:
- Coding
tags:
- php
- phpunit
---

If you look into the PHPUnit documentation ([ http://www.phpunit.de/manual/3.3/en/test-doubles.html#test-doubles.mock-objects](http://www.phpunit.de/manual/3.3/en/test-doubles.html#test-doubles.mock-objects) ) you'll see some nice examples but non of them shows how to translate a function with multiple arguments into a mock-assumption.

Within the examples you'll find:
`$observer->expects($this->once())->method('update')  
->with($this->equalTo('something'));
`

So what if the "update" function has two arguments, pretty easy:
`$observer->expects($this->once())->method('update')  
->with($this->equalTo('something'), $this->equalTo('something else'));
`

I guess Sebastian though that that there's no need for documentation if something is so obvious :(
