---
layout: post
title: "@apply to Pseudo Selectors"
tags:
  - tailwind
  - css
date: 2021-05-01 12:57 -0400
---
When `@apply` a custom component in Tailwind, the pseudo classes do not work, need to have explicit styles for `:hover` etc.

```scss
.button {
  @apply text-white bg-indigo-500 border-0 py-2 px-8 rounded cursor-pointer;

  &:focus {
    @apply outline-none;
  }

  &:hover {
    @apply bg-indigo-600;
  }
}
```