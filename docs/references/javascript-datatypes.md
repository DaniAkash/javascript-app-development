---
id: javascript-datatypes
title: Javascript Data Types
sidebar_label: Javascript Data Types
---

JavaScript provides different data types to hold different types of values. There are two types of data types in JavaScript:
- Primitive data type
- Non-primitive data type (object references)

## Primitive Data type

Primitives are known as being immutable data types because there is no way to change a primitive value once it gets created.
Primitives are compared by value. Two values are strictly equal if they have the same value.  
In JS, there are six primitive data types:

- Boolean
- Number
- String
- Null
- Undefined
- Symbol

### Boolean

A boolean represents only one of two values: true, or false. Think of a boolean as an on/off or a yes/no switch. See [`Boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) for more details.

    var x = false;  
    if (x) {  
        // this code is not executed  
    }

### Number

The number data type is used to represent positive or negative numbers with or without decimal place, or numbers written using exponential notation.

    var a = 25;         // integer
    var b = 80.5;       // floating-point number

The Number data type also includes some special values which are: Infinity, -Infinity and NaN. Infinity represents the mathematical Infinity ∞, which is greater than any number. Infinity is the result of dividing a nonzero number by 0. See [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures) for more details.

    var num2 = +Infinity;
    alert(16 / 0);  // Output: Infinity
    alert(-16 / 0); // Output: -Infinity
    alert(16 / -0); // Output: -Infinity

### String

The string data type is used to represent textual data (i.e. sequences of characters). Strings must be inside of either double or single quotes. In JS, Strings are immutable (they cannot be changed). See [`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures) for more details.

    var str1 = 'hello, it is me';  
    var str2 = "hello, it's me";

### Null

Null has one value: `null`. The value `null` represents the intentional absence of any object value.
`null` is not an identifier for a property of the global object, like _undefined_ can be. Instead, null expresses a lack of identification, indicating that a variable points to no object. In APIs, null is often retrieved in a place where an object can be expected but no object is relevant.

    // foo does not exist. It is not defined and has never been initialized:  
    foo; //ReferenceError: foo is not defined

    // foo is known to exist now but it has no type or value:  
    var foo = null;   
    foo;   
    "null"

### Undefined

A variable that has no value is undefined. `undefined` is a property of the global object; i.e., it is a variable in global scope. The initial value of `undefined` is the primitive value undefined.

A method or statement also returns `undefined` if the variable that is being evaluated does not have an assigned value. A function returns `undefined` if a value was not `returned`.

    var testVar;  
    console.log(testVar); // undefined

While it is possible to use it as an identifier (variable name) in any scope other than the global scope (because `undefined` is not a `reserved word`), doing so is a very bad idea that will make your code difficult to maintain and debug. See [`undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) for more details.

### Symbol

Symbols are new in ES6. A Symbol is a unique and immutable primitive value and may be used as the key of an Object property. See [`Symbol`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol) for more details.

    const symbol1 = Symbol();  
    const symbol2 = Symbol(42);  
    const symbol3 = Symbol('foo');  
    
    console.log(typeof symbol1);  
    // expected output: "symbol"  

    console.log(symbol3.toString());  
    // expected output: "Symbol(foo)"  

    console.log(Symbol('foo') === Symbol('foo'));  
    // expected output: false  

## Non-primitive data type

Non-primitive values are mutable data types. The value of an object can be changed after it gets created.
Non primitive values can also be referred to as reference types because they are being compared by reference instead of value.
In JS, there are three Non-primitive data types:
- Array
- Object
- Function

### Array

An array is a type of object used for storing multiple values in single variable. Each value (also called an element) in an array has a numeric position, known as its index, and it may contain data of any data type-numbers, strings, booleans, functions, objects, and even other arrays. The array index starts from 0, so that the first array element is arr[0] not arr[1].

The simplest way to create an array is by specifying the array elements as a comma-separated list enclosed by square brackets.

    var colors = ["Red", "Yellow", "Green", "Orange"];
    var cities = ["London", "Paris", "New York"];
    
    alert(colors[0]);   // Output: Red
    alert(cities[2]);   // Output: New York

### Object

The object is a complex data type that allows you to store collections of data.

An object contains properties, defined as a **_key-value_** pair. A property key (name) is always a string, but the value can be any data type, like strings, numbers, booleans, or complex data types like arrays, function and other objects. See [`object`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures) for more details.

    var emptyObject = {};
    var car = {
        "modal": "BMW X3",
        "color": "white",
        "doors": 5
    }

### Function

The function is callable object that executes a block of code. Since functions are objects, so it is possible to assign them to variables.

    var greeting = function(){ 
        return "Hello World!"; 
    }
    
    // Check the type of greeting variable
    alert(typeof greeting) // Output: function
    alert(greeting());     // Output: Hello World!