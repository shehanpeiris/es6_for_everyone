# ES6 For Everyone (Wes Bos)

Repo for me to work through Wes Bos' course: [ES6 for Everyone](https://es6.io/).

**Latest Video Watched: Module 2, Video 13, 6:51 mark**

### Module 1: New Variables

We always had `var` as a way to declare and assign variables. ES6 introduced `let` and `const` variables.

**What are the variable changes introduced in ES6?**
* Scope: (*see `var-refresher.html` file for examples*)
  * `var` variables are **function-scoped**.
    * the variable is only accessible within the function (if that's where they're declared), or globally (if not declared in a function).
  * `const` and `let` variables are **block-scoped**.
    * the variable is only accessible within the block { } in which it is declared.

* Re-Declaration:
  * `var` variables **CAN** be redeclared (e.g. `var test = 1; var test = 2`).
  * `let` and `const` variables **CANNOT** be redeclared in the same scope.

* Updating Variables:
  * `var` variables can be updated (i.e. have their values changed)
  * `let` variables are designed to be updated
  * `const` variables are designed to **NOT** be updated (i.e. they are immutable)
    * *Note: if an object is declared as a `const`, the object itself cannot be updated, but properties on the object **CAN** be updated*
        * `const shehan = {age: 29, children: 1}`
        * `shehan = {age: 30}` <- This leads to "Assignment to constant variable" error
        * `shehan.age = 30` <- This works!

* Temporal Dead Zone
  * `var` variables can be accessed at any point in the code regardless of chronological order. The value of the variable cannot be accessed unless it's requested after variable assignment. This means if there is an order of operations mistake with a `var` variable, you will not see an error message to notify you, the variable will just be `undefined`.
  * `let` and `const` variables need to be declared before they can be called in your code. If not, you will see an error message.

### Module 2: Improvements to Functions

**The Introduction of Arrow Functions**

Benefits:
  * more concise
  * implicit returns
  * anonymous functions
    * these are functions without names; typically used as an argument to other functions or as an Immediately Invoked Function Expression (IIFE)
  * doesn't rebind the value of `this`
    * with arrow functions, `this` is bound to the object in which the arrow function was defined. This means it inherits `this` from the parent object.

**Default Function Arguments**

ES6 now allows us to define default function arguments in the initial line of function definition.

*see `4-default-function-arguments.html` file for more detail**

**When NOT to use Arrow Functions**
  * when you really need `this` (e.g. adding a callback function to an event listener where you need to refer to `this` button)
  * when you are designing a method that you want bound to an object
  * when you need to build a method that is bound to a prototype
  * when you need to use the arguments object of a function

### Module 3: Template Strings

**What are the benefits of Template Strings (or Template Literals)?**

* It's a pain in the ass to mix variables and strings in JavaScript. Template Strings streamline that process by letting you write variables in the string using ``, $ and {}.
* Template literals are easier for inserting HTML markup using a string.
* We can run JavaScript code inside a template literal.
