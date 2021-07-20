---
layout: post
title: Catch-all Route
tags:
  - rails
date: 2021-04-28 12:52 -0400
---
A wildcard[^1] or a catch-all route in Rails must be near the bottom as it matches top to bottom.

```ruby
get '*tag', to: 'gifs#random'
```

Must give a name to the `*`, in this example its `tag`, which is accessible in the controller via `params[:tag]`

[^1]: [Route Globbing and Wildcard Segments - Ruby on Rails Guides](https://guides.rubyonrails.org/routing.html#route-globbing-and-wildcard-segments)