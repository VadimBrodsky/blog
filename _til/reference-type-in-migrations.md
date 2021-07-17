---
layout: post
title: Reference Type in Migrations
date: 2021-04-26 06:33 -0400
tags: rails
---
The `references` type in a migration would automatically add an index.

The `to_table` method[^1] specifies which table to use.

```ruby
t.references :follower, null: false, foreign_key: { to_table: :users }
```

[^1]: [ActiveRecord::ConnectionAdapters::SchemaStatements](https://api.rubyonrails.org/classes/ActiveRecord/ConnectionAdapters/SchemaStatements.html#method-i-add_foreign_key)
