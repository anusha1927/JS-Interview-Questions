## 1. Difference between '==' and '===' ?

- '==' are called as equality operators.
- '===' are called as strict operators.
- Equality operators just check the value where as strict operators check the value along with the data type of a variable.
- for example:
  - var a=10 \
    var b='10'\
    console.log(a==b) // true\
    console.log(a===b) // false

## 2. Difference between var, let and const ?

### Var

- can be redeclared
- can be reinitialised
- global scoped
- function scoped
- support hoisting
- introduced before ES5

### let

- cannot be redeclared
- can be reinitialised
- global scoped
- block scoped
- donot support hoisting
- introduced in ES6

### const

- cannot be redeclared
- cannot be reinitialised
- global scoped
- block scoped
- donot support hoisting
- introduced in ES6

## 3. Explain types of scopes ?

- There are 3 types of scopes

1. Global Scope

- The variables that are declared outside all the classes and fuctions. They are accessible by every function.

2. Function Scope

- The variables that are declared inside a function i.e., function test(){ //inside this }

3. Block Scope

- The variables that are declared inside a block i.e., { //inside this }. A block can be a switch, if else conditions.

## 4. What is hoisting ?

- It is a mechanism in javascript where variables and functions are moved to the top of their scope before code execution.
- In simple words, it is like used of variables or functions even before their initialisation or declaration.
- There are 2 types of hositing

  1. Function Hoisting

  - eg: a(); // called before defining the function
  -     function a(){.....}

  2. Var Hoisting

  - eg: console.log(a); // using variable 'a' before it is declared. This gives undefined.
  -     var a = 10;

- only var supports hoisting, let and const donot support hoisting.

## 5. What is TDZ ?

### Temporal Dead Zone (TDZ)

- TDZ is like when we try to access the variables before their declaration using let and const keyword then the compiler throws a reference error.
- This is introduced to improve the code quality.
- We get a "Reference Error : Cannot access 'a' before initialization"

## 6. What is first class function ?

- It is also known as function expression.
- This donot support function hoisting.
- Here it is like assigning a function to a variable.
- eg: let a = function abc(){....}

## 7. What is pure function ?

- A function which returns the same result if the same arguments (inputs) are passed in a function.
- function sum (a, b){ \
  return a\*b; \
  } \
  sum (10, 20); \
  sum (20, 20);

## 8. Explain execution context ?

### Synchronous JS

    1. Global Execution Context (GEC)
    2. Function Execution Context (FEC)
    3. Memory Allocation (MA)
        - only variables are declared and functions are defined here. Before the code execution this phase allocates memory for all the variables and functions.
    4. Code Execution (CE)
        - the variables are initialized and function calls and main execution is done here after the memory allocation.
    5. Call Stack (CS)

### Asynchronous JS

    1. Event Loop
    2. Callback Queue
    3. Call Stack
