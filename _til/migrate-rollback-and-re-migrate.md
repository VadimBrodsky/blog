---
layout: post
title: Migrate Rollback and Re-Migrate
date: 2021-04-26 06:16 -0400
tags: rails
---
Useful command[^1] to test if the custom migration is working as expected for both up and down

```bash
bin/rails db:migrate:redo

# or with step
bin/rails db:migrate:redo STEP=3
```

[^1]: [Active Record Migration - Rails Guides](https://guides.rubyonrails.org/active_record_migrations.html#rolling-back)
