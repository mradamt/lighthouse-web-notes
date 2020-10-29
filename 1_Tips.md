## TIPS
1. Use 'const' everywhere unless JS tells us not to
2. For loops:
  * for c-style: most control
  * `for...of`: used on iterable objects, like arrays
  * `for...in`: simply loops over keys of an object. DO NOT USE ON ARRAYS: it'll return the index of an array, but not guaranteed in 0->10 order.
    * Instead of `for...in`, we can use `for...of`: for `(const keys of Object.keys(obj))` OR for `(let [key, value] of Object.entries(obj))`