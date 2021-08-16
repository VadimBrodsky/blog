---
layout: post
title: React useClickOutside custom Hook
tags:
  - react
date: 2021-08-16 16:29 -0400
---
A useful custom hook to detect when a user clicked outside of an element, could be used to close a drop-down menu etc.

```javascript
import { useEffect, useRef } from "react";

export default function useClickOutside(elRef, callback) {
  const callbackRef = useRef();
  callbackRef.current = callback;

  useEffect(() => {
    const handleClickOutside = (e) => {
      if (!elRef?.current?.contains(e.target) && callbackRef.current) {
        callbackRef.current(e);
      }
    };

    document.addEventListener("click", handleClickOutside, true);
    return () => {
      document.removeEventListener("click", handleClickOutside, true);
    };
  }, [callbackRef, elRef]);
}
```

To use it:

```javascript
export default function Box() {
  const containerRef = useRef();

  useClickOutside(containerRef, () => {
    console.log("clicked outside of app");
  });

  return <div ref={containerRef>hello</div>;
}
```