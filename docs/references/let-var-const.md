---
id: let-var-const
title: Variables
sidebar_label: let, var & const
---

Informations are the building block for applications. Information is nothing but collection of data. Variables plays a vital role with respect to data.

Variable is used to store the data. In Simple terms, it can be referred as "Storage". Below are the few variable keywords in javascript used to store the data.

## Variable Keywords

var, let & const are the reserved keywords used to delcare the variables in javascript. let, const are introduced in ECMAScript 2015 (i.e ES6).

We must understand var to grasp the benefits of let and const.

## var

Variables declared with keyword var:

- by default, variables are initialized with the value undefined in javascript.

```sh
var name;
console.log(name);      // expected output: undefined
```

- have function scoped. (i.e) Variables defined inside a function are not accessible (visible) from outside the function.

```sh
var score = 50;
function myFunction() {
  var score = 74;
  console.log(score);   // expected output: 74
}
console.log(score);     // expected output: 50
```

- re-declarations of variable is possible

```sh
var name = "prasanna";  //declare and initializing the variable
var name = "balaji";    //re-declaration of same variable
console.log(name);      //balaji
```

## let

Variables declared with keyword let:

- by default, variables are initialized with the value undefined in javascript.

```sh
let name;
console.log(name);      // expected output: undefined
```

- have block scoped. A block scope is the area within if, switch conditions or for and while loops. Generally speaking, whenever we see {curly brackets}, it is a block.

```sh
let score = 50;

if (score === 50) {
  let score = 20;

  console.log(score);   // expected output: 20
}

console.log(score);     // expected output: 50
```

- Unlike var, we can't re-declare the variables using let. But, re-assigning the new value to variable is possible

```sh
let score = 40;
let score = 50;
console.log(score);     // SyntaxError: identifier "score" has already been declared.

let age = 30;
age = 40;
console.log(age);       // expected output: 40
```

## const

Variables declared with const:

- Should be initialized while declaration. Otherwise, it will throw an error.

```sh
const score = 20;
console.log(score);     //expected output: 20

const age;  // Uncaught SyntaxError: Missing initializer in const declaration
```

- Similar to let, it is block scoped.

```sh
const score = 50;

if (score === 50) {
  const score = 20;

  console.log(score);   // expected output: 20
}

console.log(score);     // expected output: 50
```

- It can't be re-assigned with new value.

```sh
const score = 30;
score = 25;    // Uncaught TypeError: Assignment to constant variable.
```

- If we declare an object with const, we can change the properties.

```sh
const Person = {
  name: 'Prasanna'
}

Person.name = 'Prasanna Balaji'
console.log(Person.name); // expected output: Prasanna Balaji
```

## Best Practices

When declaring variables, it is best practice to avoid using var. Always use let or const based on the following scenario's.

- Use let when we will be changing the value of the variable.
- Use const when we are sure that variable won't change throught the application.

Using both let and const will keep our variables in the right scope and make our code easier to manage.
