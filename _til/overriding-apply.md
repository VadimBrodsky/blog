---
layout: post
title: Overriding @apply
tags:
  - tailwind
  - css
date: 2021-04-29 12:54 -0400
---
When defining a custom Tailwind class with the `@apply` directive, it will have a higher specificity than the inline tailwind utilities.

There are 2 ways to avoid this:

1. import the `@import "tailwind/utilities"` after the custom code.
2. set `important: true` in the tailwind config[^1], this will add important to all tailwind utilities.

[^1]: [Configuration - Tailwind CSS](https://tailwindcss.com/docs/configuration#important)