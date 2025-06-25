- Main purpose of JavaScript is to implement interactiveness into webpages and web applications.
- There are three types of variables in JavaScript: `var`, `let`, and `const`
    - var (variable) was originally the only variable available.
    - Quick overview:
        - let: If a variable is going to be reassigned later in the application
        - var: Better to use let or const for variables, but this type still works. Can be updated and re-declared.
        - const: Variable will never change and will not be reassigned anywhere else in the application
    - Var is globally-scoped and can be updated and redeclared. let and const are both block-scoped, but const cannot be updated or redeclared.
    - Global scope: A variable declared outside of a function. All scripts and functions on a web application or webpage can access this variable.
    - Block scope: A variable declared inside a block. This means we can use these variables inside of loops, if statements, or other declarations within curly brackets and have them be only used for that declration instead of the entire application having access to it.
      ```
      var variableOne = 'Linus Torvalds';
      let variableTwo = 50;
      const variableThree = 'Creator of Linux Kernel';
      ```
    - Variables can store numbers, strings, and booleans. There are also other data types, such as arrays and objects. 
