---
title: 'Difference between Array and Array-like object'
date: '2021-04-12'
---

An Object which has a **length property** of a **non-negative Integer**, and usually some indexed properties. For example

```
var arraylike = {
    0:'a',
    1:'b',
    2:'c',
    length:3
};
```

It's not constructed by Array or with an Array literal [], and so (usually) **won't inherit from Array.prototype**. The length property will not usually automatically update either.

You can convert Array-like Objects to their Array counterparts using **Array.prototype.slice**

```
var arr = Array.prototype.slice.call(arraylike);   // ['a', 'b', 'c']
```

