---
layout: post
title: Vim Regex Replace to Remove Erb Tags
date: 2021-04-26 13:06 -0400
tags: vim
---

```
:s/<%=\? //
```

1. Select a block of code that came from an erb template
2. Run the ex command `:s/<%=\? //`
