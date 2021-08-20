---
layout: post
title: DOM Element Attributes
tags:
  - DOM
  - JavaScript
date: 2021-08-20 06:10 -0400
---
There are multiple ways[^1] to set and remove attributes on HTML DOM Elements:

1. `element.attributes`[^2]

> The Element.attributes property returns a live collection of all attribute nodes registered to the specified node. It is a NamedNodeMap, not an Array, so it has no Array methods and the Attr nodes' indexes may differ among browsers. To be more specific, attributes is a key/value pair of strings that represents any information regarding that attribute.

2. `element.getAttribute`[^3] and `element.setAttribute`[^4]

> The setAttribute() method sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.

> The getAttribute() method of the Element interface returns the value of a specified attribute on the element. If the given attribute does not exist, the value returned will either be null or "" (the empty string); see Non-existing attributes for details.

3. Properties on the DOM Element[^5] object, for example `element.id`[^6] or `element.className`[^7]

> The id property of the Element interface represents the element's identifier, reflecting the id global attribute.

> The className property of the Element interface gets and sets the value of the class attribute of the specified element.

[^1]: [When to use setAttribute vs .attribute= in JavaScript? - StackOverflow](https://stackoverflow.com/a/36581696)
[^2]: [Element.attributes - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/attributes)
[^3]: [Element.getAttribute() - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/getAttribute)
[^4]: [Element.setAttribute() - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)
[^5]: [Element - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element)
[^6]: [Element.id - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/id)
[^7]: [Element.className - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/className)
