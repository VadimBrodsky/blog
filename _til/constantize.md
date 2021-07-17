---
layout: post
title: Constantize
date: 2021-04-26 13:08 -0400
tags: rails
---

A method[^1] that tries to find a constant with the name specified in the argument string

```ruby
constantize('Foo::Bar') # => Foo::Bar
```

[^1]: [ActiveSupport::Inflector](https://api.rubyonrails.org/classes/ActiveSupport/Inflector.html#method-i-constantize)
