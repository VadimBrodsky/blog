---
layout: post
title: Bundle for platform
date: 2021-04-26 06:29 -0400
tags: ruby bundler
---
Add a new platform[^1] to the lockfile, re-resolving for the addition of that platform.

lock the platform

```bash
bundle lock --add-platform x86_64-linux
bundle lock --add-platform darwin
```

lock the ruby version

```bash
bundle lock --add-platform ruby
```

[^1]: [Bundler: bundle lock](https://bundler.io/v2.0/bundle_lock.html)
