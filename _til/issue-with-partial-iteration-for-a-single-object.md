---
layout: post
title: Issue with Partial Iteration for a single object
date: 2021-04-26 06:11 -0400
tags: rails
---
Partial[^1] iteration will not be defined for a single object, in the object partial.

Only the a collection is passed to `render.`

```ruby
defined?(shout_iteration)
```

[^1]: [ActionView::PartialRenderer](https://edgeapi.rubyonrails.org/classes/ActionView/PartialRenderer.html#class-ActionView::PartialRenderer-label-Rendering\+a\+collection\+of\+partials)
