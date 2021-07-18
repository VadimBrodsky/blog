---
layout: post
title: Current Model
date: 2021-04-26 06:23 -0400
tags: rails
---
A current model to track the current user etc, using the ActiveSupport::CurrentAttributes super class[^1].

> Abstract super class that provides a thread-isolated attributes singleton, which resets automatically before and after each request. This allows you to keep all the per-request attributes easily available to the whole system.



```ruby
class Current < ActiveSupport::CurrentAttributes
  attribute :user
end
```

[^1]: [ActiveSupport::CurrentAttributes](https://api.rubyonrails.org/classes/ActiveSupport/CurrentAttributes.html)
