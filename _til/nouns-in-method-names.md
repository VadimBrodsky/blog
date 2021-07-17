---
layout: post
title: Nouns in Method Names
date: 2021-04-26 13:14 -0400
tags: rails
---

A good indication that there is another object that we can extract is a tendency to add a noun into a method name.

```ruby
current_user.timeline_shouts
```

These can be extracted into different models

```ruby
@user = User.find_by(username: params[:id])
@timeline = Timeline.new([@user])
```
