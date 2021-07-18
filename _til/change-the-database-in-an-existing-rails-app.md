---
layout: post
title: Change the Database in an Existing Rails App
date: 2021-04-26 06:32 -0400
tags: rails
---
An addition in Rails 6.0 CLI command[^1] that makes it easier to change the database adapter.

```bash
bin/rails db:system:change --to=postgresql
bin/rails db:system:change --to=mysql
bin/rails db:system:change --to=sqlite3
bin/rails db:system:change --to=oracle
bin/rails db:system:change --to=frontbase
bin/rails db:system:change --to=sqlserver
bin/rails db:system:change --to=jdbc
```

[^1]: [The Rails db:system:change command - GoRails](https://gorails.com/episodes/rails-6-db-system-change-command)
