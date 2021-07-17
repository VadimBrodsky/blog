---
layout: post
title: local_assigns
date: 2021-04-26 06:13 -0400
tags: rails
---
The `local_assigns` method[^1] from `ActionView::Base` is a good way to figure out what local variables exist in a view.

```ruby
Headline: <%= local_assigns[:headline] %>
```

same as

```ruby
defined? headline && headline
```

[^1]: [ActionView::Base](https://api.rubyonrails.org/v6.1.3/classes/ActionView/Base.html#class-ActionView::Base-label-Passing+local+variables+to+sub+templates)
