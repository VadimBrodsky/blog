---
layout: post
title: Vim Sessions
tags: vim
date: 2021-07-16 18:50 -0400
---
Vim's built-in session mechanism[^1]:

> A Session keeps the Views for all windows, plus the global settings.  You can
> save a Session and when you restore it later the window layout looks the same.
> You can use a Session to quickly switch between different projects,
> automatically loading the files you were last working on in that project.

```
:h session
:h mksession
:h 'sessionoptions'
```

- To save the session `:mksession`, will save the session in a `Session.vim` file.
- To restore a session `:source ~/Session.vim` or `vim -S Session.vim`

[^1]: [Remember previous session - vi.stackexchange.com](https://vi.stackexchange.com/questions/7867/remember-previous-session)
