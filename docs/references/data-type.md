---
id: data-type
title: Data type in Javascript
sidebar_label: Data type in Javascript
---
### Data Type

A variable has the data and the variable is defined with type of data in it. A variable may be a number,letters ,etc. It is defined in type.

There are t wo types of data type.

    1. Primitive 
    2. Non - Primitive


##### Primitive Datatype
It is not object and funtion. The following data types are primitive.

	- String
	- Number
	- Boolean
	- Null
	- Undefined

##### Non-Primitive  Data

	- Object	
	- Array

##### Number

It represents integer and floating numbers.

let number = 321;
number = 321.123;
- Infinity and NAN both special numeric values belonged to number

alert( 1 / 0 ); // Infinity

alert( "a" / 2 + 1 ); // NaN

##### String

It may contain a single char or many in quotes.

let a ="Hello World";
Let b ="B";

##### Boolean

It is a logincal type. So its just have either yes or no.

let num1 =1;
let num2 =1'

(num1==num2);// true

##### Null

null does not belongs to any of the type.ype which has null. It is seperate t its just refers empty,value unknown and nothing.

let name = null;


##### Undefined

When the value is not assingned, then it is undefined.

let x;
x;//undefined

##### Non Primitive

The value after creation can be chnaged. Its mutable data type.

##### Object

It has key - value property where key is a string and balue can be any of data type.

var car = {
    "model": "Benz",
    "color": "white",
    "doors": 4
}

typeof(car); // object

var car1 ={
    "model": "Benz",
    "color": "white",
    "doors": 4
};

The objects always not true unless the object is assigned to another object.
car == car1;//false

var car2 = car;
car2 == car; //true

It is mutable type.

car.color ="Black";

##### Array

It is sequenticial data. The index starts from 0. The data type can be anything inside array.

var colors =["Red","Blue","White"];
colors[0];//Red