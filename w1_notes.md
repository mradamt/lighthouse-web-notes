# COMMAND LINE ARGUMENTS
* Cmd line args are passed as strings to a program

### Output format
In node, using process.argv, args start from 'node' so the fun starts from process.argv[2]. So output of `node [program] [one two three]`:
  ```
  0 -> /home/vagrant/.nvm/versions/node/v10.20.1/bin/node
  1 -> /vagrant/w1/d1-focal/processargv.js
  2 -> one
  3 -> two
  4 -> three
  ```


# BOOTCAMP BASICS
## Groundrules TRAVIS
Lectures are conversations!
Ask questions by unmuting, or zoom chat, or zoom gestures

### Bootcamp vs CS
CS trains students in a lot of math and theory, but doesn't produce good developers at graduation. Bootcamps do developer training... (silence on the math and theory training)
Interview differences: person with degree will have a better understanding of architecture?
* Interviews vary
* Given some data and we need to remember x, y, z, how would you store this data most efficiently in a DB?
CS students will have lots more experience with the algorithms, data structures etc. Bootcampers will have far more familiarity with dev workflows, git, writing clean code that integrates with tests, passing code to seniors for review. Big tech is becoming less afraid of bootcamp grads, mainly if you can prove your credentials and your talents you should be fine. 

Travis notes that he's not actually feeding us kool-aid, he's a CS grad, both have their benefits. 

### Timeline
Weeks 1-5: FOCAL
Weeks 7-11: Web frameworks etc.
Week 6 and Weeks 11-12 are project weeks, no lectures.

## Incremental code
**Break the problem down into smaller, easier to understand, _isolated_ (if possible) steps.** Much easier in these cases to isolate erros, and refactor code in the future. 



# DATA TYPES AND OBJECTS
## Groundrules ANDY
Prefers to call lectures 'conversations'
Instruction: Don't take notes.

### Compass
Request assistance frequently: like, daily


## Primitive data types
The value itself is stored in memory
The values are immutable. The values aren't 'changed', they are replaced.

Note that objects are not. So even a const object can be modified.
Primitive types are passed into functions as the data itself, i.e. a copy. Objects are passed by reference so the object itself is mutable. Check [pythontutor.com](pythontutor.com) to visualize.


## Levels of abstraction
It's perfectly fine to not understand the depths of why the computers do what they do. Understanding just **that** it works can be enough, aim to understand what's needed and be careful of slowing learning by obsessing over deeper layers.


## Objects
* In JavaScript there are primitive data types, and everything else is an object.




# CALLBACKS AND ARROW FUNCTIONS
# Callbacks
(These are hard, give yourself time to figure it out)

Callback: function passed as a parameter and used by another function

## Function declaration vs expression
Functional expressions force better programming practices.

This is because of hoisting. Functions are hoisted in JS, so functions can be called before their declarations, which is a confusing way to sequence a program. E.g. when reviewing code, I don't know if this func is native, or pulled in from somewhere else etc.

So using functional expressions means functions can not be called until the function expression is written. 


## Arrow functions
* Arrow functions change how the `this` keyword works. When using a method we need to be careful with how we use `this`.




# DEPENDENCIES
## Dependencies
`npm install` saves any specified packages into `dependencies` by default.
Additionally, you can control where and how they get saved with some additional flags:
[npm-install docs](https://docs.npmjs.com/cli/v6/commands/npm-install)


What does `--save-dev` (`-D`) do during `npm install [package] -D`? ---
  It saves the dev dependencies of the package you're installing. 
  Dev dependencies are packages you rely on to DEVELOP your app, but aren't required by users to actually run the app in production. This'll include things like testing packages, you only test in DEV not PROD, so test packages will live in the `package.json` file as `devDependencies`.

