---
layout: post
title: Checking Syntax in Ruby
tags:
  - ruby
  - cli
date: 2021-04-24T14:08:55.992Z
---

To check if a given Ruby file has any syntax errors:

```shell
ruby -cw file.rb
```

Using the flags:
- `c` to check
- `w` for extra warnings
