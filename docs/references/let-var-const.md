---
id: let-var-const
title: Let,Var and Const
sidebar_label: Let,Var and Const
---
### Variables in Javascript

In Javascript, var is used to declare variables. ES6 introduces two other keywords declaring block scope varoables. The block scope variable are having the scope only inner most block which can be the block having curly brackets.The three identifiers have few singnificant variance each other.

#### Understanding let

1. let does not have a property to add global objects

Example:

    var x =10;
    console.log(window.x); //10

    let y = 11;
    console.log(window.y); //undefined

2. let is block scope rather than Global scope

Example:

    function([array of args])
    {
    //i available here
    for (var i=0;i<=[array of args].length;i++)
    {
    //some code
    }
    //i available here
    }


    function([array of args])
    {
    //i is not available here
    for (let i=0;i<=[array of args].length;i++)
    {
    //some code
    }
    //i is available here
    }

3. Redeclaration is not possible.

Example:
    var a=10;//10
    var a=11;//11

    let a=10;//10
    let a =10;//Uncaught SyntaxError: Identifier 'a' has already been declared


#### Understanding const

const is a keyword since ES6. it cannot be change once after the declaration.

    let x = 10;                                           
    x = 20;
    // console.log(x) => 20 

    const x = 10;
    x = 20;
    //  Uncaught TypeError: Assignment to constant variable.


const does not make objects immutable. 

    const phone= { name: 'iPhone', series: '7' }
    phone.series = '8'   
    console.log(phone)   
    //   { name: 'iPhone', series: '8' }


    const phone= Object.freeze({ name: 'iPhone', series: '7' })//freeze makes objects immutable
    phone.series = '8'   
    console.log(phone)   
    //   { name: 'iPhone', series: '7' }
