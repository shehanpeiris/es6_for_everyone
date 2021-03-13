# ES6 For Everyone (Wes Bos)

Repo for me to work through Wes Bos' course: [ES6 for Everyone](https://es6.io/).

### Module 1: New Variables
**What are the variable changes introduced in ES6?**
We always had `var` as a way to declare and assign variables. ES6 introduced `let` and `const` variables.

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




