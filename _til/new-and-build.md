---
layout: post
title: ActiveRecord New and Build
tags: rails active_record
date: 2021-04-17T15:04:32.799Z
---

In the past[^1] the difference between ActiveRecord `build` and  ActiveRecord `new` was that the former would create associations while latter didn't. This is no longer the case[^2] as:

```ruby
alias build new
```

[^1]: [What is the difference between build and new on Rails - StackOverflow.com](https://stackoverflow.com/questions/1253426/what-is-the-difference-between-build-and-new-on-rails/1253462#1253462)
[^2]: [rails/activerecord/lib/active_record/relation.rb - Github.com](https://github.com/rails/rails/blob/9a263e9a0ffb82faa6d3153fd1f35b814a366cd5/activerecord/lib/active_record/relation.rb#L79)
