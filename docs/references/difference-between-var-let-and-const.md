---
id: difference-between-var-let-and-const
title: Difference Between Var, Let and Const
sidebar_label: Difference Between Var, Let and Const
---

Most of the beginners often get confused with the three keywords var, let and const as they are specific to Javascript. So, let's have a clear understanding of it.

## var

This can have two types of scopes for a variable called `Global scope` and `Function Scope` but misses `Block Scope`. Global Scope is where we declare/define a variable outside of a function block. Function scope is defined inside a function block. Block scope is defined only within a block of code (i.e. within a pair of curly brackets ). 

These var keywords are processed by the Javascript compiler before the code gets executed. Hence they are positioned at the top of its scope which is called `Hoisting`.

Using the var keyword, it is optional to initialize the variable with a value. Redeclaring the same variable is posobjectsible as it overrides the previous one.


```
var a = 10

function foo(){
    console.log(b) // undefined
    var b = 5
    console.log(b) // 5

}

foo()
console.log(a) // 10
var a= 6
console.log(a) // 6
console.log(b) // Uncaught ReferenceError: b is not defined

```

## let

ES6 introduced let keyword which removes the limitations caused by hoisting. With let we can declare `block-scoped` variables. Redeclaring the same variable will raise a `SyntaxError`.

Similar to var, the variable can be optionally initialized to a value. Let will also hoist the variable to the top of the block. However, referencing the variable before it is declared results in `RefernceError`.

```
let x = 2
let x = 1 // Uncaught SyntaxError

function foo(){
    console.log(b) // Uncaught ReferenceError
    for 
    let b = 5
    console.log(b) // 5
}

x = 10
console.log(x) // 10

```

## const

Keyword const is used to hold a `constant value` that can never be changed. Similar to let, const also has a `block-scope`.

const cannot be redeclared or reassigned to a new value. This is beacuse const creates a read-only reference to a value. It doesn't mean that the value is immutable. `Primitive values` (string, number, boolean, null, undefined) are `immutable` while the `non-primitive values` (object, array, function) are `mutable`.

Non

```
const favLang = "JS"
const favLang = "python" // Uncaught SyntaxError

favLang = "php" // Uncaught TypeError

const arr = [1,2,3]
arr.push(4)
console.log(arr) // [1,2,3,4]
arr.pop()
console.log(arr) // [1,2,3]

const arr = ["JS","C","C++","JAVA"] // Uncaught SyntaxError

```



