---
layout: post
title: Random Order in ActiveRecord Query
tags:
  - rails
  - active_record
date: 2021-04-28 12:46 -0400
---
Can use a SQL `RANDOM` function in the Active Record `order` method[^1].

```ruby
Gif.tagged_with(params[:tag]).order('RANDOM()').first
```

[^1]: [ActiveRecord::QueryMethods#order](https://api.rubyonrails.org/classes/ActiveRecord/QueryMethods.html#method-i-order)