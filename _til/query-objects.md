---
layout: post
title: Query Objects
date: 2021-04-26 13:26 -0400
tags: rails
---

- Connecting more complex SQL statement together
- Can be placed in `/app/queries`

```ruby
class ShoutSearchQuery
  def initialize(term:)
    @term = term
  end

  def to_relation
    Shout.joins(
      'LEFT JOIN text_shouts ON content_type = "TextShout" AND content_id = text_shouts.id',
      )
      .where('text_shouts.body LIKE ?', "%#{term}%")
      .order(created_at: :desc)
  end

  private

  attr_reader :term
end
```
