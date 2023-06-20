## Q1. Difference between “ == “ and “ === “ operators.

Both are comparison operators and they return boolean values always. The difference
between both the operators is that “==” is used to compare values whereas “ === “ is
used to compare both value and datatype.


```bash
let a=10
let b="10"
 console.log(a==b)// true

 let a=10
let b="10"
 console.log(a===b)// false
  
```
---
## Q2. What are the differences between var, let and const?

### var - 
    1. It can be redeclare and reinitilized
    2. Global scope and Function Scope
    3. Hoisting can be performed
    4. Used before introduce ES6
    
```bash
example - 
var b =10
var b=20
console.log(a)// 20

```
    
  
### let
    1. not Redeclare and reinitilized
    2. no Hoisting
    3. Block scope, Global Scope
    4. TDZ
    5. introduce in ES6
    
```bash

example - 
let a =120
a=10
console.log(a)//10
```
### const
    1. not Redeclare and Not reinitilized 
    2. no Hoisting
    3. Block scope, Global Scope
    4. TDZ
    5. introduce in ES6



## Type of Scope
1. Global Scope
- The Javascript global scope is the context where everything in a Javascript program executes by default. This scope includes all variables, objects, and references that are not contained within a customized scope defined by a programmer. Global scope is the entire Javascript execution environment.
2. Function Scope

- JavaScript has function scope: Each function creates a new scope. Variables defined inside a function are not accessible (visible) from outside the function. Variables declared with var , let and const are quite similar when declared inside a function.

```bash
var ABC = 10;
let PQR = 20;
const XYZ = 30;
function funcScope(){
    var ABC = 100;
    let PQR = 200;
    const XYZ = 300;
    console.log(ABC); // 100
    console.log(PQR); // 200
    console.log(XYZ); // 300
}
funcScope()

console.log(ABC); //10
console.log(PQR); //20
console.log(XYZ); //30
```

3. Block Scope
- The block scope of a variable means that the variable is accessible within the block that is between the curly braces.

```bash
{
    var ABC = 100;
    let PQR = 200;
    const XYZ = 300;
    console.log(ABC); // 100
    console.log(PQR); // 200
    console.log(XYZ); // 300
}

console.log(ABC);  // 100
console.log(PQR); // not define - error
console.log(XYZ); // not define - error

```
---
## Q3. Hoisting 
-  
    1. Function Hoisting
    - Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution. Inevitably, this means that no matter where functions and variables are declared, they are moved to the top of their scope regardless of whether their scope is global or local.

    ```bash
     Abc();
    function Abc(){
    console.log("Section!!!");//Section!!!
    }  
    ```

    2. var keyword Hoisting
    - Hoisting is the js mechanism where var and function declaration are moved to top of their scope before code execution.

```bash
       console.log(a)// undefined
       var a=10
```
---
## Q4. What is a Temporal Dead Zone (TDZ)?
- 
     when trying to acceess a variable before it's decleration with let and const keyword.

- introduce to imporve the code quality by detecting & preventing to use variable.
- A temporal dead zone (TDZ) is the area of a block where a variable is inaccessible until the moment the computer completely initializes it with a value.
---
## Q5. What is meant by first class functions?
- Assign a function to a variable is first class function.

```bash
      let P = function Sum(){
    console.log("Hi");
    return "Hello"
    }

    console.log(P());
```
---
## Q6 . Pure Function 
- A pure function in JavaScript is a function that returns the same result if the same arguments(input) are passed in the function.
```bash
function Sum(a, b){
    return a * b;
}

Sum(10, 20)
Sum(20, 20)
Sum(20, 30)
```
---




