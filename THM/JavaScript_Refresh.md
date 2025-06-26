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

## JavaScript Cheatsheet
#### Arithmetic Operators
| Operator | Type | Use Case & Example |
| --- | --- | --- |
| + | Addition | Addition, add numbers or strings together. 25 + 5 = 30 |
| ++ | Increment | Increase variable by 1, so let x=20; x++; x=21 |
| - | Subtraction | Subtract the variable's numbers, 15-5=10 |
| -- | Decrement | Decrease variable's number by 1, so let x=20; x--; x=19 |
| * | Multiplication | Multiplies one number ny another, 5 * 10 = 50 |
| / | Division | Divides one number by another 100/10 = 10 |
| % | Modulus | Returns remainder, 100 % 8 = 4 |

#### Comparison Operators
| Operator | Use Case & Example |
| --- | ---|
| == | Equal to, 100 == 100 |
| === | Equal to & identical, 500 === 500 (looking for identical types) | 
| != | Not equal to, 100!=50 |
| !== | Not identical, 35!==75 |
| < | Less than, 5 < 85 |
| <= | Less than or equal to, 60 <= 90 |
| > | Greater than 30 > 5 |
| >= | Greater than or equal, 1,000>= | 

#### Data Types
| Data Types | Example |
| --- | --- |
| String | 'Morpheus' |
| Arrays | [1,2,3] |
| Objects | {Name:'John', Occupation:'Master Hacker'} |
| Booleans | True or false |
| Numbers | 455 |
| Floating-point numbers | 10.5 |

## Conditionals 
```
if (5 === 5) {
console.log('Hello world!'); // Prints to console
};
```

```
if (5 === 10) {
console.log('Hello world!'); // Skips this
} else if (10 === 10) {
console.log('Hello World!'); // Prints hello world to the console!
};
```

```
if (5 === 10) {
console.log('Hello World!'); // Skips this code
} else if (10 === 10) {
console.log('Hello world!);
} else {
console.log('ERROR');
};
```

## Switch Cases
```
const animal = 3;
switch (animal) {
case 1:
document.write('Cow');
break; \\ Ending specific case/switch block
case 2:
document.write('Chicken');
break;
case 3:
document.write('Monkey');
break;
default: \\ In case our variable is equal to something not present in our switch
dcoument.write('Animal?'); }
```

## Functions
- 
