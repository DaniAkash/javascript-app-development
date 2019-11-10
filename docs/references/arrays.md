---
id: arrays
title: Arrays
sidebar_label: Arrays
---
An array is a global object that can hold a list of elements of any data type and access them by a single variable.

### Array Declaration
There are basically two ways to declare an array.
- With the literal notation `[ ]`
```
let myHobbies = ["Dancing","Singing","Programming","Cooking","Writing"]
```
- With the array `constructor`
```
let shirtSize = new Array(34,36,38,40,42,44,46)
```
### Array Methods
### push()
### pop()
### shift()
### unshift()
### reverse()
### find()
It is used to create a new object based on the condition you set. On the surface, it looks like filter() but they’re not the same. filter() returns an array of matched objects while find() will return the first matched object.
```

```
### every()
### concat()
### slice()
### splice()
### filter()
It is a method that lets you create a new array based on conditions that evaluate to true from an existing array.
```
const marks = [85,76,93,88,95,79]
const filteredMarks = marks.filter(mark =>{
    return mark>80
})
console.log(filteredMarks) // [85,93,88,95]
```
### map()
### reduce()

### Summary of commonly used array methods

| Method | Description |
| ------ | ----------- |
| push(...items) | Inserts an element at the end |
| pop() | Removes an element at the end and returns it |
| shift() | Removes the first element |
| unshift(..items) | Inserts an element at the beginning |
| forEach(func) | Calls a function for each element in the array |
| filter(func) | Creates a new array based on conditions that evaluate to true from an exisiting array |
| map(func) |  Creates a new array with the results of calling a provided function on every element in this array |
| reduce(func,initial) | Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value |
| concat(...items) | Creates a new array containing all the elements in the original array followed by the each of the arrays that are passed in |
| slice(start,end) | Extracts a section of an array and returns a new array excluding the end position |
| splice(pos,n,...items) | At index pos, delete 'n' elements and insert items |
| find(func) | Returns the first matched object |
| every(func) | Returns a boolean value true or false value based on the conditions set |
| some(func) | Returns true if at least one of the condition evaluates to true |
| reverse() | Reverses the array in-place and returns it |
| join(optional seperator)| Concatenates all the members of an array into a string, along with a separator |
| toString() | Joins an array together into a string by comma separator |

For more details on Javascript array methods visit <u>[MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Static_methods)</u>