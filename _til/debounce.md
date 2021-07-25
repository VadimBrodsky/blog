---
layout: post
title: Debounce
tags:
  - javascript
date: 2021-07-25 06:44 -0400
---
Tried to reimplement the debounce function today, pretty fun. The trick is to handle the `timeoutId` correctly, and cancel any previous invocations so only the last one remains.


```javascript
/*
 * Creates and returns a new debounced version of the passed function
 * which will postpone its execution until after wait milliseconds
 * have elapsed since the last time it was invoked.
 */
export default function debounce(fn, time) {
  let timeoutId;

  const debouncedFn = (...args) => {
    if (timeoutId) {
      clearTimeout(timeoutId);
    }

    timeoutId = setTimeout(() => {
      fn.apply(this, args);
    }, time);
  };

  debouncedFn.cancel = () => {
    clearTimeout(timeoutId);
  };

  return debouncedFn;
}
```

This implementation is not too dissimilar to what underscore does[^1], just with some extra options.

The Lodash debounce implementation[^2] is very hard to follow, maybe because its all in one file :shrug:

[^1]: [Underscore debounce.js - Github](https://github.com/jashkenas/underscore/blob/master/modules/debounce.js)
[^2]: [Lodash debounce function - Github](https://github.com/lodash/lodash/blob/4.17.15/lodash.js#L10304)