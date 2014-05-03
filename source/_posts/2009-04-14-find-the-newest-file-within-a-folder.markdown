---
author: tolleiv
comments: true
date: 2009-04-14 20:14:42+00:00
layout: post
slug: find-the-newest-file-within-a-folder
title: find the newest file within a folder....
wordpress_id: 3
tags:
- bash
- shell
---

These are two neat little commands to find the newest and oldest file within a folder and it's subfolder:
` find . -type f -printf "%T@ %p \n" | sort -n -k 1,1 | awk '{print $2}' | tail -n 1
find . -type f -printf "%T@ %p \n" | sort -n -k 1,1 | awk '{print $2}' | head -n 1`
If you'd like to know how old/young these files are try these two:
`find . -type f -printf "%T@ %C+ %p \n" | sort -n -k 1,1 | tail -n 1
find . -type f -printf "%T@ %C+ %p \n" | sort -n -k 1,1 | head -n 1`

I hope that's a good starter for the "blog" :P
