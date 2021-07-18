---
layout: post
title: First or Initialize
date: 2021-04-26 06:15 -0400
tags: rails
---

If not sure if already have a record. The `first_or_initialize` method[^1] is good to avoid duplication. A close relative is the `find_or_create_by` method[^2]

```ruby
twitter_account = Current
  .user.twitter_accounts
  .where(username: auth.info.nickname)
  .first_or_initialize
```

[^1]: [first_or_initialize - apidock.com](https://apidock.com/rails/v6.1.3.1/ActiveRecord/Relation/first_or_initialize)
[^2]: [ActiveRecord::Relation#find_of_create_by](https://api.rubyonrails.org/classes/ActiveRecord/Relation.html#method-i-find_or_create_by)
