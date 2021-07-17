---
layout: post
title: Counter Cache to Optimize Queries
date: 2021-04-26 12:57 -0400
tags: rails
---

Rails has a neat feature to cache counters[^1] for associations.

```ruby
belongs_to :author, counter_cache: true
```

- Need to add a column `books_count` for that to work.
- Or specify a specific column instead:

```ruby
belongs_to :author, counter_cache: :count_of_books
```

[^1]: [Options for belongs_to - Rails Guides](https://edgeguides.rubyonrails.org/association_basics.html#options-for-belongs-to)
