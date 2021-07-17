---
layout: post
title: Model Single Responsibility
date: 2021-04-26 13:19 -0400
tags: rails
---

Sometimes using a model inside another model can be a red flag:

```ruby
def timeline_shouts
  Shout.where(user_id: followed_user_ids + [id])
end
```

Good questions to ask:
- should this live in the User model?
- should this live in the Shout model?
- is there a different domain object that can be extracted to better encapsulate this concept?
