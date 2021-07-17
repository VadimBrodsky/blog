---
layout: post
title: safe_join
date: 2021-04-26 05:58 -0400
tags: rails
---

This method[^1] returns an HTML safe string similar to what `Array#join` would return. The array is flattened, and all items, including the supplied separator, are HTML escaped unless they are HTML safe, and the returned string is marked as HTML safe.

```ruby
safe_join(list, ', ')
```

[^1]: [ActionView::Helpers::OutputSafetyHelper](https://api.rubyonrails.org/v6.1.3.1/classes/ActionView/Helpers/OutputSafetyHelper.html#method-i-safe_join)

