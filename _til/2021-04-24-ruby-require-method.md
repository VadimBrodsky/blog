---
layout: post
title: Ruby Kernel#require Method
tags: ruby
date: 2021-04-24 06:21 -0400
---
The Ruby `Kernel#require` method[^1]:
- If `require` is called more than once with the same arguments it would not be reloaded if its already loaded.
- Ruby keeps track of which files were already required.
- Usually you don't need the extension when `require`ing a feature.

The `Kernel#require_relative` method[^2] is very similar to `require`:
- Behaving the same just in the same directory as the file that the code is executing from.
- Don't need to manipulate the load path to get to the current folder

[^1]: [module Kernel#require - RubyDoc](https://docs.ruby-lang.org/en/3.0.0/Kernel.html#method-i-require)
[^2]: [module Kernel#require_relative - RubyDoc](https://docs.ruby-lang.org/en/3.0.0/Kernel.html#method-i-require_relative)
