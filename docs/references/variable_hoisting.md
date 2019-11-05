# Variable Hoisting
>  In JavaScript Hoisting is a mechanism by default which moves all the variables and function declaration to the top of their scope before code execution

Let us see what the above lines actually means
*For example,*
```javascript
console.log(pokemon);    //Output : ReferenceError: pokemon is not defined
```
In the above example we try to print out the value of variable pokemon which is not declared before. We will get a error message as output saying **Reference error** pokemon is not defined. ( Note : reference error in javascript is thrown when we try to access the previously undeclared variable )
```javascript
console.log(pokemon);   //output : undefined
var pokemon = "pikachu";
```
But in this case we wont get the reference error instead of that we get undefined which means the variable has been declared but it is not assigned to any value.
> This is where the Hoisting concept comes to play what it actually do is that
- First it reads your program file before loading it to run the program.
- While reading the program whenever it reads the var keyword it put all those variable to the top of that particular scope.
- Below is how the code will change after the reading of the program completed.

```javascript
var pokemon;
console.log(pokemon);    // undefined
var pokemon = "pikachu";
```
So this is how all the variables will be declared on top of the scope after reading the program file. That is why we are getting undefined as output.
*Another example,*
```javascript
console.log("name of the cat is ", cat);    // name of the cat is undefined
console.log("name of the mouse is ", mouse);    // name of the mouse is undefined
var cat = "Tom";
var mouse = "Jerry";
```
So as of now we have seen the concept of variable hositing with some basic example

------------


Let us seen some real time situation where this  actually matters
```javascript
var DEFAULT_SCORE = 100;
var score = 200;
function getScore(){
if (!score){
var score = DEFAULT_SCORE;
}
return score;
}

console.log("Team Score : ",getScore());  
   
// Expected output : Team Score : 200
// Actual output : Team Score : 100
```
   
> In this example,
- we defined two variables DEFAULT_SCORE and score at the start of the program
- Then we create a getScore function in which
     - if condition will execute only when score is undefined or null and then assign the score variable to DEFAULT_SCORE value
     - Else it will return the previously assigned value 200

But we are getting 100 as output instead of 200, this is because of hoisting.
 **Below snippet shows how browser see your code after reading the program**
```javascript
var DEFAULT_SCORE = 100;
var score = 200;
function getScore(){
var score;    // score was initialized and it is undefined
if (!score){
var score = DEFAULT_SCORE;    // now score is set to 100  
}
return score;
}          

console.log("Team Score : ",getScore());  
   
// output : Team Score : 100
```
  **Explanation : **
- In `line no 6` var keyword is used since we know var is a function scope instead of a block scope
- It means var is not scoped under the block if statement instead it has it's scope under the function getScore
- As we saw in our previous example whenever var keyword is used it is put on top of **their scope ** while reading
- That's why var score is placed on top of its function scope not on top of the block scope of "if" statement where it is actually declared and assigned to DEFAULT_SCORE
- This is one of the main issue in hoisting
To overcome this issue we can use this following methods :

## Strict Mode
In ES5 version Strict mode was introduced. By using Strict mode our browser will not accept the usage of a variable before they are declared.
For example,
```javascript
'use strict';
console.log(pokemon); // Output : ReferenceError: pokemon is not defined
pokemon = 'pikachu';
```
## LET and CONST
In ES6 version let and const keyword were introduced for declaring variables in javascript like var keyword.
The advantage of using let and const is that they are block scoped not a function scoped like var

**Let**
```javascript
console.log(pokemon); // Output: ReferenceError: pikachu is not defined ...
let pokemon = 'pikachu'
```
**Const**
const differs from let keyword it is not only block scoped it's values cannot be changed.
```javascript
console.log(pokemon); // Output: ReferenceError: pikachu is not defined ...
const pokemon = 'pikachu'
```
## Summary
- Hoisting issues are difficult to debug.
- To overcome this issue strict mode, let and const are used.
- Try to minimize the usage of var keyword to declare a variable instead of that use let and const keyword for declaration to avoid this hoisting probelm