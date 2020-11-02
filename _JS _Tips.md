## Secret gist std
// secretGist name: lhl-w0XdY--fileName.js

## TIPS
1. Use 'const' everywhere unless JS tells us not to
2. For loops:
    * for c-style: most control
    * `for...of`: used on iterable objects, like arrays
    * `for...in`: simply loops over keys of an object. DO NOT USE ON ARRAYS: it'll return the index of an array, but not guaranteed in 0->10 order.
      * Instead of `for...in`, we can use `for...of`: for `(const keys of Object.keys(obj))` OR for `(let [key, value] of Object.entries(obj))`
3. Primitives vs objects:
    * Primitives are referenced by value
      * When the primitive is copied, its value is stored in the copy. The copy is otherwise not related to the original.
    * Objects are referenced by pointer/address
      * When the object is copied, its reference is stored in the copy. So both the copy and the original store the object's address, the **object** isn't duplicated so all we've done is created two variables that can operate on the same object.
    * To create a deep copy of an object we can use 
      * spread `objCpy = {...obj}`
      * assign `Object.assign(objCpy, obj)`
      BUT note that these only true-copy the first layer of `obj`: any object values that are objects themselves will be copied by the above methods **by refrence**
4. Javascript culls extra parameters when functions are called with more arguments than parameters:
    * `function twoParams(one, two) = {return 'something'}`
    * 
    * 
5. `process.stdout.write()` == `console.log` but without the \n new line char
6. Arrow functions don't have their own `this`. This is useful! Say you have a method that calls `array.forEach(function())`, without arrow functions we couldn't include `this` in our `forEach()` call! See [this example](https://javascript.info/arrow-functions#arrow-functions-have-no-this).
7. 

