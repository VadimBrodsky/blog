---
layout: post
title: Ruby Kernel#load Method
tags: ruby
date: 2021-04-24 06:15 -0400
---
The Ruby `Kernel#load` method[^1]:
- Executed at the point where Ruby encounters it in the file.
- Can load files that the names are determined dynamically during the execution of the program.
- Calls to `load` can also be conditional.
- Giving the `load` fully qualified path would bypass the load path.
- A call to `load` loads the file even if it was already loaded, overwriting the things loaded in the previous versions.

[^1]: [module Kernel#load - RubyDoc](https://docs.ruby-lang.org/en/3.0.0/Kernel.html#method-i-load)
