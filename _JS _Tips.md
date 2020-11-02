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

## PAPER NOTES
1. `if (condition) {take this action}`
  1. Ternery: `boolean test ? action if true : action if false`
2. Falsy values:
  * false
  * 0
  * null
  * "" empty string
  * undefined
  * NaN
3. Arrow functions (see notes above about 'this' with arrow funcs):
  1. `const variable = (a, b) => {return something using a and b}`
  1. `const variable = () => {return something}`
  1. `const variable = a => {return something using a}`
  1. `const variable = a => something using a`
4. Switch statements:
  ```switch (condition) {
    case 'thisCase':
      doSomething;
      break;
    case 'anotherCase':
      doSomethingElse;
      break;
    default:
      doDefaultIfNoOtherCasesMatch;
  }
5. Default parameters
  1. `function name(x = 'someDefaultValue') {return something using x; the default value will be used if no x is provided as an argument}`
    * `name(a) --> does things to 'a'`
    * `name() --> does things to 'someDefaultValue'`
6. Block scope: the code within {}
  * Best practice is to avoid the global namespace
  * Also best practice to avoid reusing variable names
7. `for...in` vs `for...of` ---> `for PROPERTY in object` :::: `for ELEMENT of array`