---
id: Data-types
title: Javascript Data Types
sidebar_label: Javascript Data Types
---

JavaScript provides different data types to hold different types of values. There are two types of data types in JavaScript:
- Primitive data type
- Non-primitive data type (object references)

The fundamental difference between primitives and non-primitives is that primitives are immutable and non-primitives are mutable.
Primitives are known as being immutable data types because there is no way to change a primitive value once it gets created.

## Primitive Data type
In JS, there are six primitive data types:

- Boolean
- Number
- String
- Null
- Undefined
- Symbol

### Boolean

A boolean represents only one of two values: true, or false. Think of a boolean as an on/off or a yes/no switch.

> var x = false;  
        if (x) {  
        // this code is not executed  
        }

### Number

There is only one type of Number in JavaScript. Numbers can be written with or without a decimal point. A number can also be +Infinity, -Infinity, and NaN (not a number).

>    var num1 = 32;  
    var num2 = +Infinity;

### String

Strings are used for storing text. Strings must be inside of either double or single quotes. In JS, Strings are immutable (they cannot be changed).

>    var str1 = 'hello, it is me';  
     var str2 = "hello, it's me";

### Null

Null has one value: `null`. The value `null` represents the intentional absence of any object value.

>   // foo is known to exist now but it has no type or value:  
    var foo = null;   
    foo;   
    "null"

### Undefined

A variable that has no value is undefined.

>    var testVar;
    console.log(testVar); // undefined

### Symbol

Symbols are new in ES6. A Symbol is an immutable primitive value that is unique. For the sake of brevity, that is the extent that this article will cover Symbols.

> const mySymbol = Symbol('mySymbol');