---
id: var-let-const
title:  Understanding of Var, Let and Const
sidebar_label: Var, Let & Const
---

End of this article you will know the difference between var, let & const, Why should we move on to let & const over var, also a bit of intro about hoisting and scopes.

Before dive into the topic understanding of variable declaration vs initialization, scopes, and hoisting will provide a better understanding.

## Variable declaration vs initialization

The creation of a variable without assigning its value is called a **variable declaration**. In JavaScript, if variable declared without its value by-default it will be considered as `undefined` 

    var user;  //undefined

Similarly whenever a variable created with its own value is called **variable initialization** or variable assignment.

One way of doing it is directly assigning a value when it is declared.

    var user= "John";  //John

We can also initialize value after variable declaration.

    var user;  //undefined
    user= "John"  //John

## Scope

Scope in JavaScript refers to the current context of code, which determines the accessibility of variables to JavaScript. The following are the types of scopes in JavaScript

1. Global Scope
2. Local Scope
    - Function Scope
    - Block Scope

### Global Scope Vs Local Scope

In **Global Scope**, variables are declared globally on top of the function or block. Which can be accessed anywhere in the program except functions which has a local variable scope inside a function.

In **Local Scope**, variables are declared locally inside a function or block. Those local variable dies once the function or block executed. There is no scope outside

Let's see an example to understand the global and **function scope**.

    var user = "John";  //Initialized a Global Variable
    
    function aka() {
    	var user = "Johnson";  //Initialized Function Scoped a Local Variable
    	console.log(user);
    }
    
    //Lets console both global and local variable
    console.log(user);
    aka();
    console.log(user);
    
    ----------------------------------------------------------
    output:

    John
    Johnson
    John

In the above example if you see we declared `user` variable twice as a global *`(John)`* and local variable *`(Johnson)`* inside a function. The local scope doesn't affect the global scope as it ends once the function executed.

Similarly, let's see an example of a **block scope**. *(here will take let instead of var since let is block scoped)*

    	let user = "John";  //Initialized a Global Variable
    		if(user){
    			let user = "Johnson"; //Initialized a Block Scoped a Local Variable
    			console.log(user);
    		}
    	console.log(user);
    
    ----------------------------------------------------------
    output:

    Johnson
    John

In the above example, we can see block-scoped variables don't affect our global scope. If we used `let` inside any of the blocks { `if, else` } or loops {`for, while.. etc)`} its scope lies within that block only.

## Hoisting

The process of assigning variable declarations a default value of `undefined` during the creation phase is called Hoisting.

Before execution of code JavaScript engine will look for all the variables and functions in the entire code to allocate memory and a default value `undefined`.

Lets understand with an example
```
    var name = "John";
    var role= "Web Dev"
    
    function person() {
    	console.log(name+role);
    }
    
    person();
    
    ----------------------------------------------------------
    output:
    
    John Web Dev
```
Let's see what browser knows before the line by line execution
```sh
    name : undefined;
    role : undefined;
    person : fn()
```
With the above note if any variable or function called before executing the declaration line we will get the output of `undefined` as it is assigned before the execution process start.

Lets call a variable before declared and see what happens

    console.log(name);
    person();
    var name = "John";
    var role= "Web Dev"
    
    function person() {
    	console.log(role);
    }
    ----------------------------------------------------------
    output:
    
    undefined
    undefined

If you see the output is `undefined` since we called before the declaration of the variable

Since we understood variable declaration, variable initialization, scopes, and hoisting. Understanding of Var, Let & Const would be easy for us.

## Var

- Function Scoped /  Current Execution Context
- `undefined` when accessing a variable before it's declared ***(Hoisting)***
- Can be redeclared
- Can be reassigned
- Initializing with value is optional
- Create a property on the global window object

## Let

- Block Scoped
- `Reference Error` when accessing a variable before it's declared ***(No-Hoisting)***
- Cannot be redeclared (in the same scope)
- Can be reassigned
- Initializing with value is optional
- Does not create a property on the global window object

## Const

- Block Scoped
- `Reference Error` when accessing a variable before it's declared ***(No-Hoisting)***
- Cannot be redeclared (in the same scope)
- Cannot be reassigned

    Non- Primitives like Arrays can be changed by  its method ( push, pop ) as well as assigning new values to exist properties and adding new properties in Objects are possible ( Basically once const variables declared we cannot change its Reference )

    - Must be initialized with a value
    - Does not create a property on the global window object

## Best Practices

Before Let and Const introduced in ES6 everyone used Var, however, which has some drawbacks like hoisting and accidental reassign of variables, which produces unnecessary bugs also fixing those bugs is a headache when it comes to the large codebase.

Below are the best practices to maintain a clean code.

- Always use const as first priority
- Use Let where you can't use const (Mostly when your code requires reassignment)
- Try to avoid using var completely