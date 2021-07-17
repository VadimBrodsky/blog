---
layout: post
title: Polymorphic belongs_to in Fixtures
date: 2021-04-26 06:20 -0400
---
Pretty nice syntactic sugar[^1] to add polymorphic relations in fixtures:

```ruby
belongs_to :eater, polymorphic: true
```

In the fixture:

```yaml
apple:
  eater: george (Monkey)
```

Same as:

```yaml
apple:
  id: 1
  name: apple
  eater_id: 1
  eater_type: Monkey
```

[^1]: [ActiveRecord::FixtureSet](https://api.rubyonrails.org/classes/ActiveRecord/FixtureSet.html#class-ActiveRecord::FixtureSet-label-Polymorphic+belongs_to)
