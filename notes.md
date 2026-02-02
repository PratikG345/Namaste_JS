Everything in Js happens inside an `execution` context. Its a big box where your code is executed and variables, functions, and objects are stored. 

- 1st component is memory component where variables and functions are stored. 
- heavy word is `Variable Environment`.

Javascript is a `synchronous` `single-threaded` language. It means it can do `one thing` at a time.


## What happens when you run Javascript Program?

```
var n=2;
function square (num){
    var abs = num * num;
    return ans;
} 
var square2 = square(n);
var square2 = square(4);
```

the execution context created in 2 phases:
* Memory Creation Phase
* Code Execution Phase


| Memory | Code |
| --- | --- |
| n: undefined | |
| square: function square (num) {---} | | 
| square2: undefined | | 
| square4: undefined | | 

functions are a heart of javascript.

## Hoisting
Hoisting is a phenomenon is javascript where you can **access variables and functions** even **before you have initialized** it.

Even before the code is executed, memory is assigned to each variable and function.


if we make a function as **arrow function**, it would **act as a variable** and not as a function, and would **store undefined** instead of entire function.

## Window : 
Window is a global object which is created along with the global execution context

whenever we created a execution context, the `this` object is created with it, which **points to window**.

```
this === window // true
```

## Global space : 
Any thing we write or any variable we define which is not inside a function is in global space


how to access variables in global space?
```
x = 10
console.log(window.x) // 1
console.log(x) // 2
console.log(this.x) //3
```

## Undefined vs Not Defined in JS

**Undefined :** A placehoder used by js to assign to a varaible which is **not been assigned** yet.

```
console.log(a) // undefined
var a = 7
var b;
console.log(a) // 7
console.log(b) // undefined
```

**Not Defined :** If a variable is **not yet declared** and is logged, it throws a variable not defined error.
```
console.log(x) // Error : x is not defined.
```

JS is  `loosely-typed` language.