---
layout: post
title: new RegExp and Strings in JavaScript
tags:
  - javascript
  - regexp
date: 2021-08-15 06:39 -0400
---
When creating a regular expression in JavaScript from a string, the backslashes are consumed[^1] which can lead to subtle bugs:

```javascript
new RegExp("\d")    // > /d/
new RegExp("\d\w")  // > /dw/ 
```

There are a couple ways to avoid this, using a second backslash `//` or using the `String.raw` method[^2]:

```javascript
new RegExp("\\d\\w\\s")         // > /\d\w\s/
new RegExp(String.raw`\d\w\s`)  // > /\d\w\d/
```

[^1]: [Escaping Special Characters in new RegExp - JavaScript.info](https://javascript.info/regexp-escaping#new-regexp)
[^2]: [String.raw - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/raw)

