## Secret gist std
// secretGist name: lhl-w0XdY--fileName.js

## TIPS
1. Use 'const' everywhere unless JS tells us not to
2. For loops:
    * for c-style: most control
    * `for...of`: used on iterable objects, like arrays
    * `for...in`: simply loops over keys of an object. DO NOT USE ON ARRAYS: it'll return the index of an array, but not guaranteed in 0->10 order.
      * Instead of `for...in`, we can use `for...of`: for `(const keys of Object.keys(obj))` OR for `(let [key, value] of Object.entries(obj))`
      * `for...in` vs `for...of` ---> `for PROPERTY in object` :::: `for ELEMENT of array`
4. Javascript culls extra parameters when functions are called with more arguments than parameters:
    * `function twoParams(one, two) = {return 'something'}`
5. `process.stdout.write()` == `console.log` but without the \n new line char



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
7. 