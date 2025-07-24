# _JavaScript_


_JavaScript was introduced by **Netscape** in 1995 as a lightweight scripting language to enhance web pages with interactivity, allowing code to run in the user's browser alongside **HTML** and **CSS**._

_In 1997, it was standardized as **ECMAScript** through the ECMA-262 specification, maintained by **ECMA International**. This specification established the core features of the language, ensured consistent implementation across browsers, and continues to evolve through regular updates that expand and improve the standard._

_Today, JavaScript has grown into a powerful and versatile language employed in many different environments, such as :_

* :globe_with_meridians:  _**Front-end** frameworks (React)_ 
* :gear: _**Back-end** development (Node.js)_
* :iphone: _**Mobile apps** (React Native)_
* :desktop_computer: _**Desktop apps**_
* :satellite: _**IoT** (Internet of Things)_
* :robot: _**AI**/**ML** (Artificial Intelligence / Machine Learning)_
* :video_game: _**Games**_

## _Overview_

_JavaScript is a **high-level**, **dynamic** programming language that is **interpreted**, meaning its code is executed line by line at runtime without the need for prior compilation. As a dynamic language, JavaScript allows variables to change types freely, and many decisions about behavior and structure are made while the program is running._

_JavaScript supports multiple programming paradigms, including **object-oriented**, **functional** and **procedural** styles, giving developers the flexibility to choose the approach that best fits their needs. It is both dynamically and **weakly typed** (variables do not require explicit type declarations, and their types can change during execution)._

_JS code runs inside an environment called the **JavaScript engine**, which is most commonly found in web browsers (these engines read and execute the code, enabling web pages to respond to user actions in real time). Beyond browsers, JS can also run on servers, desktops and even small devices thanks to platforms like Node.js. This versatility allows developers to use the same language to build a wide range of applications._

## _Syntax information_

_Although it is not mandatory to end statements with a semicolon, it is good practice to always include closing punctuation._

_JavaScript is **case sensitive**, which means it distinguishes between uppercase and lowercase._

_Like any language, JavaScript provides character sequences to insert **comments** into the code. Anything marked as a comment is ignored by the JavaScript interpreter. We can insert two types of comments into the code :_ 

* _```single-line comment``` : begins with the characters ```//```_
* _```multi-line comment``` : starts with the sequence ```/*``` and ends with ```*/```_

_Whitespace in JS has no special meaning in expressions and we can use it to improve the **readability** of our code._

## _Variables_

_A variable is a container that holds a value. There are three main ways to declare variables in JS :_

* _```let```: for variables that can change. It is **block-scoped** (exists only inside the {} block where they are defined)._
* _```const```: for variables that must not change. It is **block-scoped**._
* _```var```: the old way (avoid using it). It is **function-scoped** (exists in the whole function)._
 
_Variables declared outside any function or block are considered **global** and can be accessed throughout the entire program, including inside functions and blocks, unless shadowed by a local variable with the same name. Variables declared inside a function or block are **local** to that scope and cannot be accessed from the outside._

<sub>When declared globally, **let** and **const** create variables that are not added to the **global object**, whereas **var** does.<sub>

_The **global object** is the top-level object in JavaScript that represents the global scope. In browsers, it is referred to as **window**, while in Node.js it is known as **global**. Variables declared with **var** at the global level become properties of the global object, meaning they can also be accessed via **window.variableName** (in browsers) or **global.variableName** (in Node.js), whereas variables declared with **let** and **const** do not attach themselves to this object._

## _Operators and Expressions_

_An expression is any code that produces a value._

_Operators perform actions on values (operands). They are grouped into categories :_

* _**Arithmetic Operators** (used for basic math) :_

  - _**Addition** : ```+```_
  - _**Subtraction** : ```-```_
  - _**Multiplication** : ```*```_
  - _**Division** : ```/```_
  - _**Modulus** (remainder) : ```%```_
  - _**Exponentiation** : ```**```_
  - _**Increment** : ```++```_
  - _**Decrement** : ```--```_

  _<sub>The increment and decrement operators can be used in two forms : **prefix** (```++x``` in this case the variable is updated first, then used) and **postfix** (```x++``` the variable is used first, then updated).<sub>_

* _**Assignment Operators** (used to assign or update values in variables) :_

  - _**Assign** : ```=```_
  - _**Add and Assign** : ```+=```_
  - _**Subtract and Assign** : ```-=```_
  - _**Multiply and Assign** : ```*=```_
  - _**Divide and Assign** : ```/=```_
  - _**Assign the remainder** : ```%=```_
  - _**Assign the exponential** : ```**=```_
  
* _**Comparison Operators** (used to compare two values, returns true or false) :_

  - _**Equal** : ```==```_
  - _**Equal** (strict : compares both value and type) : ```===```_
  - _**Not Equal** : ```!=```_
  - _**Not Equal** (strict) : ```!==```_
  - _**Greater than** : ```>```_
  - _**Less than** : ```<```_
  - _**Greater than or Equal** : ```>=```_
  - _**Less than or Equal** : ```<=```_
  
* _**Logical Operators** (used with boolean values) :_
  
  - _**AND** : ```&&```_
  - _**OR** : ```||```_
  - _**NOT** : ```!```_
  
* _**String Operator** (used to join strings - concatenation) : ```+```_
  
* _**Type Operators** :_
   - _```typeof``` : returns type of value_
   - _```instanceof``` : checks if value is an instance of a class_
  
## _Data Types_

_Data types define the kind of value a variable can hold. JavaScript is a **dynamically typed language**, meaning you don't need to declare the type of a variable (it is determined automatically at runtime)._\
_Despite being flexible, JS still enforces rules based on the type of the data we are working with (these rules affect how values behave, how operations are performed and how values are compared)._

_JavaScript data types are divided into two main categories :_

* _**Primitive Types** :_
  
  _**Basic**, **immutable** values (once a primitive value is created, it cannot be altered; however, the variable holding it can be reassigned to a new value). These values are stored directly in memory and **compared by value**, not by reference._
  
    - _```string```: a **sequence of characters** delimited by double or single quotes (it is possible to insert special characters inside a string by using the escaping character ```\``` )._
  
    - _```number```: includes both **whole numbers** and **decimals**; in addition to the classic base ten notation, we can represent numbers in **octal** (the number starts with ```0```) and **hexadecimal** notation (the number starts with ```0x```). Any value that goes outside the representable range does not generate an exception but is represented by two special values : **Infinity** and **-Infinity**._
  
      _<sub>Another special numeric value is **NaN** (Not a Number) which indicates an undefined numeric value.<sub>_
  
  - _```bigint```: used for very **large integers**, beyond the number limit._
  - _```boolean```: **True** or **False** values._
  - _```undefined```: a variable that has been declared but not given a value._
  - _```null```: rapresents an intentional **empty value**._
  - _```symbol```: creates a unique, unchangeable value, used as object property keys._
  
* _**Non-Primitive Types** (Objects) :_
  
  _Complex types like **arrays**, **functions** and **objects** (**mutable** and stored **by reference**)._

### _Template Literals_

_Template literals provide an easy and readable way to create strings with embedded expressions._

_Instead of quotes (```'``` or ```"```) use **backticks `**, and embed expressions inside **${}**._

_```const name = "Bob";```_\
_```const age = 25;```_

_Traditional concatenation :_\
_```const message1 = "My name is " + name + " and i am " + age + " years old.";```_

_Using template literals :_\
_```const message2 = `My name is ${name} and i am ${age} years old.`;```_

## _Type Conversion_

_JavaScript supports :_ 

* _**Implicit Conversion** : JS automatically converts types when needed (it is not always safe)._
* _**Explicit Conversion** (Manual) :_

  - _Convert to **String** :_

    + _```String(value)```_
    + _```value.toString()```_
      
  - _Convert to **Number** :_
  
    + _```Number(value)```_
    + _```parseInt(value)``` or ```parseFloat(value)```_
    
    _<sub>It stops at the first invalid character, for example if we have ```value = "123abc"``` the result of ```parseInt(value)``` would be ```123```.<sub>_
    
    + _Unary Plus Operator : ```+value```_
    
    _<sub>Converts the operand to a number exactly like ```Number(value)```, if the value can't be converted to a valid number it returns **NaN**.<sub>_
  
  - _Convert to **Boolean** : ```Boolean(value)```_

## _Arrays_

_An **array** is a special variable that can hold multiple values in an **ordered collection**, where each value, called an **element**, is accessed by a **zero-based index** (starting at 0). Arrays can contain **heterogeneous data types** (elements within the same array can be numbers, strings, objects, or even other arrays) and can **dynamically grow or shrink in size**._

_To create arrays in JavaScript there are two main ways :_ 

* _**Array Literal** :_

  - _```const numbers = [10, 20, 30]```_
  - _```const fruits = ["apple", "peach", "orange"]```_
  - _```const mixed = [1, "hi", true]```_

* _**Array Constructor** :_

  - _```const arr1 = new Array(3)``` : creates an empty array of length 3._
  - _```const arr2 = new Array(1, 2, 3)``` : creates ```[1, 2, 3]``` cause when the array constructor is used with multiple arguments each argument becomes an element in the new array._
 
_To **access** and **modify** array elements we use its **zero-based index** : ```array[index]```._

_```const colors = ["red", "green", "blue"];```_\
_```console.log(colors[0]);``` output : "red"_\
_```colors[0] = "black";```_\
_```console.log(colors[0]);``` output : "black"_

_<sub>Accessing an index outside the array bounds returns **undefined**.<sub>_\
_<sub>Assigning a value to an index beyond the current length increases the array size, filling missing elements with **undefined**.<sub>_

## _Control Flow_

_Control Flow determines the order in which the code executes. JavaScript provides several structures to control this flow, allowing programs to **make decisions** and **repeat tasks** efficiently._

### _Code Blocks_

_A code block is a group of one or more statements enclosed within curly braces ```{ }```. It allows multiple statements to be treated as a single unit, meaning all the code inside the braces is executed together as a block. Those blocks help **organize** code logically and improve **readability** and **maintainability** by clearly grouping related instructions._

### _Conditional Statements_

_They allow a program to make decisions and execute certain blocks of code based on specific conditions. JavaScript provides several forms to implement **decision-making** logic :_

* _**if** : executes a block of code if a specified condition evaluates to ```true```._

  ```let x = 15;```\
  ```if (x > 10){```\
  ```  console.log("true");```\
  ```}```
  
* _**if...else** : provides an alternative block of code to execute when the condition is ```false```._

  _```let x = 15;```_\
  _```if (x > 10){```_\
  _```  console.log("true");```_\
  _```} else {```_\
  _```  console.log("false");```_\
  _```}```_

* _**Ternary Operator** : a compact syntax for simple **if...else** conditions._

  _```condition ? expressionIfTrue : expressionIfFalse;```_

  _```let x = 15;```_\
  _```let check = x > 15 ? true : false;```_
  
* _**else if** : checks multiple conditions in sequence, the first that evaluates to ```true``` is executed._

  _```let x = 15;```_\
  _```if (x > 30){```_\
  _```  console.log("option 1");```_\
  _```} else if (x > 20) {```_\
  _```  console.log("option 2");```_\
  _```} else if (x > 10) {```_\
  _```  console.log("option 3");```_\
  _```} else {```_\
  _```  console.log("option 4");```_\
  _```}```_

* _**switch** : is used to perform different actions based on the value of a variable or expression. It's often used as a cleaner alternative to multiple **if...else if** conditions, especially when checking the same variable against many different values._

  _```switch (expression) {```_\
  _```  case value1:```_\
    _```    // Code to run if expression === value1```_\
    _```    break;```_\
  _```  case value2:```_\
    _```    // Code to run if expression === value2```_\
    _```    break;```_\
  _```  default:```_\
    _```    // Code to run if none of the above cases match```_\
  _```}```_

  _<sub>The **break** statement stops the switch from continuing to the next case<sub>_\
  _<sub>The **default** case is optional and runs only if no other case matches<sub>_

### _Loops_

_Loops execute a block of code multiple times, based on a fixed number of iterations or while a specified condition remains true. This mechanism automates repetitive tasks and reduces code duplication._

* _**for** : repeats code a predeterminated number of times, it consists of three parts within parentheses : **initialization**, **condition** and **increment**._

  _```for (let i = 0; i < 5; i++) {```_\
  _```  console.log("iteration number :", i);```_\
  _```}```_

  _<sub>**Initialization** : sets the starting value (let i = 0)<sub>_\
  _<sub>**Condition** : checks whether the loop should continue (i < 5)<sub>_\
  _<sub>**Increment** : updates the counter after each iteration (i++)<sub>_

* _**while** : continues executing as long as its condition evaluates to ```true```. The condition is checked before each iteration._

  _```let count = 0;```_\
  _```while (count < 5) {```_\
  _```  console.log("count is:", count);```_\
  _```  count++;```_\
  _```}```_

  _<sub>To prevent an infinite loop, it is necessary to modify the variable involved in the condition within the loop body.<sub>_

* _**do...while** : ensures that the code block runs at least once, as the condition is evaluated only after the initial execution._

  _```let number = 0;```_\
  _```do {```_\
  _```  console.log("Number is:", number);```_\
  _```  number++;```_\
  _```} while (number < 3);```_

* _**for...of** : is used to iterate over **iterable objects**, such as arrays, strings and more. It retrieves the values of the iterable one by one._

  _```for (const element of iterable) {```_\
  _```  //code block using element```_\
  _```}```_

  _<sub>**iterable** refers to any object that implements the iterable protocol (arrays, strings..).<sub>_\
  _<sub>**element** represents the current value being accessed in each iteration.<sub>_

* _**for...in** : is used to iterate over the **enumerable properties** (keys) of an object._

  _```for (const key in object) {```_\
  _```  //code block using key and object[key]```_\
  _```}```_

  _<sub>**object** refers to the target object whose properties are being iterated.<sub>_\
  _<sub>**key** represents each property name (as a string) on the object.<sub>_

_JavaScript offers two important statements to control the flow inside loops :_

  * _**break** : immediately **terminates** the loop in which it is placed, and trasfers control to the first statement following the loop._\
  * _**continue** : **skips** the current iteration of the loop and moves to the next one immediately._

_These statements help manage how and when a loop stops or skips iterations, providing flexibility in looping logic._
  
## _Functions_

_A function is a set of instructions enclosed in a block of code that performs a specific task. It is identified by a **name**, can accept **arguments** (input parameters), and can **return** a value._\
_Functions allow the grouping of related operations into a reusable unit, improving modularity, reducing repetition, and enabling abstraction._

### _Function Declaration_

_A function can be declared using the ```function``` keyword, followed by a name, a parameter list in parentheses (optional), and a block of code enclosed in curly braces._

_```function greet(){```_\
_```  console.log("Hello world!");```_\
_```}```_

_Declaring a function does not execute it immediately. In fact, the declaration simply registers the function with the JavaScript engine, associating the given name with a specific block of code that can be executed later by calling the function._

```greet();```

### _Parameters and Arguments_

_Functions can be defined to accept **parameters**, which act as placeholders for values that will be provided during function execution. When the function is called, **arguments** are passed to replace the parameters._

_```function greet(name) {```_\
_```  console.log("Hello, " + name);```_\
_```}```_

_```greet("Alice");```_  

_<sub>"Alice" is the argument passed to the parameter "name"<sub>_

_If fewer arguments are passed the missing parameters will be ```undefined```. Extra arguments are ignored unless explicitly handled._

_It's also possible to assign **default** values to function parameters directly in function declaration. This means if a value isn't provided when the function is called, the default will be used._

_```function myFunc(param1 = defaultValue1, param2 = defaultValue2){}```_

_Inside every **non-arrow** function, a special object called ```arguments``` is available. It contains all the arguments passed to the function, regardless of the number of parameters declared._\
_It is an **array-like** object, in fact it has indexed elements and a **length** property, but it is not a real array and therefore lacks array methods like **.map()** or **.forEach()**._

_```function sum(){```_\
_```  let z = 0;```_\
_```  let i;```_\
_```  for (i in arguments){```_\
_```    z += arguments[i];```_\
_```  }```_\
_```  return z;```_\
_```}```_

_This object is useful when it's unclear how many arguments a function will receive. Instead of fixing the number of parameters, it allows the function to collect any number of arguments, making it more flexible and reusable._

_In modern JavaScript, the **rest parameter** (**...**) offers a cleaner and more powerful alternative to the arguments object. It allows a function to collect all remaining arguments into a real array, enabling the use of array methods like **.map()**, **.forEach()**, and **.reduce()**._\
_Unlike **arguments**, the rest parameter works in both arrow and regular functions, and provides better readability and control when working with an unknown number of arguments._

_```function sum(...numbers){```_\
_```  let total = 0;```_\
_```  for (let num of numbers){```_\
_```    total += num;```_\
_```  }```_\
_```  return total;```_\
_``` }```_

_It's possible to use the **rest** operator to collect only a part of the arguments into an array, allowing separation of specific parameters from the rest._

_```function showColors(firstColor, secondColor, ...otherColors) {```_\
_```  console.log("First :", firstColor);```_\
_```  console.log("Second :", secondColor);```_\
_```  console.log("Others :", otherColors);```_\
_```}```_

_```showColors("red", "blue", "green", "yellow", "purple");```_

### _Return Statement_

_The **return** statement is used in functions to send a value back to the place where the function was called. When a function reaches a return statement, it stops executing and returns the specified value._\
_Without a return statement, a function returns **undefined** by default._

_```function multiply(a, b){```_\
_```  return a * b;```_\
_```}```_

_```const result = multiply(4, 5);```_\
_```console.log(result);```_

_<sub>The multiply function calculates the product of two numbers and returns the result. The returned value is then stored in the variable result and printed to the console.<sub>_

### _Arrow Functions_

_Arrow functions are a shorter syntax for writing functions in JavaScript, they are especially useful for writing concise, anonymous functions._

_**Regular Function** :_

  _```function add(a, b) {```_\
  _```  return a + b;```_\
  _```}```_

_**Arrow Function** :_

  _```const add = (a, b) => {```_\
  _```  return a + b;```_\
  _```};```_

_If the function has only **one expression**, it's possible to omit both the braces and the **return** keyword :_

  _```const add = (a, b) => a + b;```_

_If there is only **one parameter**, i'ts possible to omit the parentheses :_

  _```const square = x => x * x;```_
  
_If there are **no parameters**, empty parentheses are used :_

  _```const sayHi = () => console.log("Hi!");```_

_Arrow Functions lack their own **this** (which is inherited from the surrounding scope) and **arguments** objects (using rest parameter is used to handle arguments), they also cannot be used as constructors with **new**._ 

### _Function Expression_

_Is a function defined as part of an expression. Essentially, the function (**anonymous** or **named**) is assigned to a variable or constant._

 _```const functionName = function() {```_\
 _``` ...body...```_\
 _```};```_

 _Or with a named function expression._

 _```const p = function positive(n) {```_\
 _``` return n > 0 ? true : false;```_\
 _```};```_

### _Anonymous Functions_

_In **JS**, a function can either be **named** or **anonymous**. While named functions have an identifier by which they can be referenced and reused, anonymous functions do not have a name. They are defined without an identifier and are typically used in places where functions are used only **once** or **in-line**, such as callbacks or function expressions._\
_An anonymous function cannot be directly referenced elsewhere in the code unless it is **assigned to a variable** or passed as a **parameter** to another function._

_Some of the most typical uses include :_

* ***Function Expressions***

  _```const add = function(a, b) {```_\
  _``` return a + b;```_\
  _```};```_

_<sub>The function is created anonymously and assigned to a constant, which acts as its reference<sub>_

* ***Callbacks***

  _```const numbers = [1, 2, 3];```_

  _```const squares = numbers.map(function(num) {```_\
  _``` return num * num;```_\
  _```});```_

_<sub>Anonymous functions are ideal as arguments to higher-order functions like ```map()```, ```filter()```, ```forEach()```, or event handlers.<sub>_

* ***Event Listeners***

  _```document.querySelector("#btn").addEventListener("click", function() {```_\
  _``` alert("Button clicked!");```_\
  _```});```_


_With the introduction of **ES6**, **arrow functions** became a common way to write anonymous functions more concisely._

_```const multiply = (a, b) => a * b;```_

_<sub>Arrow functions are always anonymous unless assigned to a variable or used as part of an object property or class method.<sub>_

_They are especially common in callbacks :_

_```const evens = [2, 4, 6];```_\
_```evens.forEach(num => console.log(num));```_

### _Callback Functions_

_In **JS**, a **callback function** is a function provided as an argument to another function, which is then executed at a specific point in time. This mechanism enables the definition of custom behavior that is triggered after a particular task has completed or when a certain condition is met._

_The callback pattern is central to asynchronous programming, where operations such as event handling, timers, or data fetching occur independently of the main execution flow._\
_A callback is not a unique type of function but rather a conventional function used in a specific role. Instead of embedding fixed behavior within a function, a separate function can be passed in to determine what should happen once the primary task finishes. This approach promotes code modularity and reusability, as one function focuses on performing the task while the callback determines the post-task logic._

_Callbacks can operate either synchronously or asynchronously. Synchronous callbacks are executed immediately during the execution of the outer function (commonly seen in array methods like ```map```, ```forEach```, or ```filter```) while asynchronous callbacks are deferred until a future time, such as after a delay using ```setTimeout``` or upon completion of a network request or user interaction._


### _Built-in Functions_

_Also called **predefined functions**, are standard functions provided by the JavaScript environment to perform common tasks. These functions are available by default and do not require manual definition._

* ***Output & Utility Functions***
  
  - _```console.log()``` : outputs a message to the console._
    
    _<sub>console.log("Message")<sub>_
    
  - _```alert()``` : shows an alert dialog._

    _<sub>alert("Message")<sub>_
    
  - _```confirm()``` : shows a confirmation dialog._

    _<sub>confirm("Are you sure?")<sub>_
    
  - _```prompt()``` : shows an input dialog._

    _<sub>prompt("Enter your name")<sub>_
    
  - _```typeof()``` : returns the type of a variable._

    _<sub>typeof 123 --> "number"<sub>_   
    
* ***Number and Math Functions***
  
  - _```parseInt()``` : converts a string to an integer._

    _<sub>parseInt("42") --> 42<sub>_
    
  - _```parseFloat()``` : converts a string to a floating-point number._

    _<sub>parseFloat("4222") --> 4.22<sub>_
    
  - _```isNaN()``` : checks if a value is NaN._

    _<sub>isNaN("abc") --> true<sub>_
    
  - _```isFinite()``` checks if a value is a finite number._

    _<sub>isFinite(20) --> true<sub>_
    
  - _```Math.round()``` : rounds to the nearest integer._

    _<sub>Math.round(5.8) --> 6<sub>_
    
  - _```Math.floor()``` : rounds down to the neares integer._

    _<sub>Math.floor(5.8) --> 5<sub>_
    
  - _```Math.ceil()``` : rounds up to the nearest integer._

    _<sub>Math.ceil(5.2) --> 6<sub>_
    
  - _```Math.abs()``` : returns the absolute value._

    _<sub>Math.abs(-6) --> 6<sub>_
    
  - _```Math.pow()``` : raises to a power._

    _<sub>Math.pow(2, 3) --> 8<sub>_
    
  - _```Math.sqrt()``` : returns the square root._

    _<sub>Math.sqrt(25) --> 5<sub>_
    
  - _```Math.max()``` : returns the largest value._

    _<sub>Math.max(5, 7, 3, 1) --> 7<sub>_
    
  - _```Math.min()``` : returns the smallest value._
 
    _<sub>Math.min(5, 7, 3, 1) --> 1<sub>_
    
  - _```Math.random()``` : returns a random number between 0 and 1._

    _<sub>Math.random() --> 0.20<sub>_

* ***String Functions***

  - _```String()``` : converts any value to a string._

    _<sub>String(123) --> "123"<sub>_
    
  - _```toUpperCase()``` : converts a string to uppercase._
 
    _<sub>"hello".toUpperCase() --> "HELLO"<sub>_
    
  - _```toLowerCase()``` : converts a string to lowercase._
 
    _<sub>"Hello".toLowerCase() --> "hello"<sub>_
    
  - _```trim()``` : removes whitespace from both ends of a string._
 
    _<sub>"   hey ".trim() --> "hey"<sub>_
    
  - _```includes()``` : checks if a string contains a substring._
 
    _<sub>"JavaScript".includes("Script") --> true<sub>_
    
  - _```substring()``` : Returns a portion of the string starting from the start index up to but not including the end index (if start > end the method swaps them automatically, also negative values are treated as 0)._

    _<sub>"Hello".substring(1, 4) --> "ell"<sub>_
    
  - _```replace()``` : Replaces the first occurrence of searchValue in the string with newValue._
 
    _<sub>"Hello".replace("l", "r") --> "Herlo"<sub>_
    
  - _```split()``` : splits a string into an array using a specified separator, and optionally limits the number of splits. If the separator is an empty string, the result is an array of characters; if the separator is not found, the entire string is returned as a single-element array; if the separator is omitted, the result is an array containing the original string as a single element._
 
    _<sub>"a,b,c".split(",") --> ["a", "b", "c"]<sub>_

* ***Array functions***

  - _```Array.isArray()``` : checks if a value is an array._
 
    _<sub>Array.isArray([3, 4]) --> true<sub>_
    
  - _```push()``` : adds elements to the end of an array._
 
    _<sub>[3, 4].push(5) --> [3, 4, 5]<sub>_
    
  - _```pop()``` : removes the last element._
 
    _<sub>[3, 4, 5].pop() --> 5 (returns the removed element)<sub>_
    
  - _```shift()``` : removes the first element._
 
    _<sub>[3, 4, 5].shift() --> 3 (returns the removed element)<sub>_
    
  - _```unshift()``` : adds elements to the beginning._
 
    _<sub>[4, 5].unshift(3) --> [3, 4, 5]<sub>_
    
  - _```splice()``` : changes an array by removing a specified number of elements starting at a given index, and optionally inserting new elements at that position._
 
    _<sub>[1, 2, 3].splice(1, 1, "a", "b") -->  [2] (returns the removed element) and changes the array in [1, "a", "b", 3]<sub>_

    _<sub>[1, 2, 3].splice(2, 0, 4, 5) --> [] cause nothing was removed, anyway the array changes in [1, 2, 3, 4, 5].<sub>_

    _So the first parameter is the start index, the second represents how many elements to remove, and the others specify the elements to insert._
    
  - _```slice()``` : returns a shallow copy of part of an array from the start index (inclusive) to the end index (exclusive)._
 
    _<sub>[1, 2, 3].slice(0, 2) --> [1, 2]<sub>_
    
  - _```join()``` : joins array elements into a string, separated by a specified separator._
 
    _<sub>[1, 2, 3].join("-") --> "1-2-3"<sub>_

    _If no separator is provided, elements are joined with a comma by default._

  - _```indexOf(element)``` : returns the index of the **first occurrence** of **element** in the array, or -1 if not found._
 
    _<sub>[1, 3, 9, 4].indexOf(9); --> 2<sub>_

  - _```includes(element)``` : returns **true** if the element exists in the array, otherwise **false**._
 
    _<sub>[1, 4, 2, 5].includes(2); --> true<sub>_

  - _```forEach(callback)``` : executes the **callback** function on each element of the array (returns nothing)._
 
    _<sub>arr.forEach(el => console.log(el));<sub>_

  - _```map(callback)``` : creates a new array by applying the **callback** function to every element._
 
    _<sub>let squares = arr.map(x => x * x);<sub>_

  - _```filter(callback)``` : creates a new array with elements that pass the test implemented by **callback**._
 
    _<sub>let bigNumbers = arr.filter(x => x > 5);<sub>_

  - _```reduce(callback, initialValue)``` : processes an array and reduces it to a single value by applying a **callback function** on each element, one by one._
 
    _<sub>array.reduce((accumulator, currentValue, index, array) => { }, initialValue);<sub>_

    _**Accumulator** : the result of the previous callback iteration (or **initialValue** on the first run);_\
    _**CurrentValue** : the current element being processed;_\
    _**Index** (optional) : the index of the current element;_\
    _**Array** (optional) : the array on which **reduce** is called;_\
    _**InitialValue** : the starting value for the accumulator._

    _<sub>const numbers = [1, 2, 3, 4];<sub>_\
    _<sub>const sum = numbers.reduce((acc, curr) => acc + curr, 0);<sub>_\
    _<sub>console.log(sum); output : 10<sub>_

* ***Timing Functions***

  - _```setTimeout()``` : executes a function after a delay. It returns an **ID** that identifies the timer._

    _<sub>const timerID = setTimeout(() => {...}, 1000)<sub>_
    
  - _```setInterval()``` : repeats a function at regular intervals. It returns an **ID** that identifies the interval._
 
    _<sub>const intervalID = setInterval(() => {...}, 1000)<sub>_
    
  - _```clearTimeout()``` : cancels a timeout previously set with **setTimeout()** using its **ID**._
 
    _<sub>clearTimeout(timerID)<sub>_
    
  - _```clearInterval()``` : cancels an interval previously set with **setInterval()** using its **ID**._
 
    _<sub>clearInterval(intervalID)<sub>_

### _Function Prototype Chain_

_In JS, functions are objects, more specifically, they are **first-class objects** (or **first-class citiziens**). This means they can be **stored in variables**, **passed as arguments** to other functions, **returned** from functions, and even assigned properties and methods, just like any other object._\
_This is possible because functions in JavaScript are actually instances of the built-in **Function** constructor, and **Function** itself inherits from **Object**._

_This is what allows functions to access special methods like ```.call()``` or ```.bind()``` (defined on **Function.prototype**), as well as generic object methods like ```.toString()``` (defined on **Object.prototype**)._

#### _Function.prototype Methods_

_Every function in JS inherits from **Function.prototype**, which provides several built-in methods. These methods allow functions to be manipulated and invoked in flexible ways._

* _**call(thisArg, ...args)** : allows to invoke a function while explicitly setting the **this** context, and to pass arguments one by one._

  _```function sayHello(){```_\
  _``` console.log(`Hello, my name is ${this.name}`);```_\
  _```}```_

  _```const person = {```_\
  _``` name : "Alice"```_\
  _```};```_

  _```sayHello.call(person);``` output : Hello, my name is Alice_

  _<sub>Here, **this.name** refers to **person.name** cause person has been passed as **thisArg**.<sub>_

  _```function greet(greeting, punctuation) {```_\
  _``` console.log(`${greeting}, my name is ${this.name}${punctuation}`);```_\
  _```}```_

  _```const user = {```_\
  _``` name : "Bob"```_\
  _```};```_

  _```greet.call(user, "Hi", "!");``` output : Hi, my name is Bob!_

* _**apply(thisArg, argsArray)** : similar to **call()**, but arguments are passed as an array._

  _```function introduce(age, city) {```_\
  _``` console.log(`I'm ${this.name}, ${age} years old from ${city}.`);```_\
  _```}```_

  _```const user = {name : "Bob"};```_

  _```introduce.apply(user, [30, "Rome"]);``` output : "I'm Bob, 30 years old from Rome."_
  
* _**bind(thisArg, ...args)** : creates a new function with a fixed **this** value and optionally pre-set initial arguments. Unlike **call()** and **apply()**, it does not invoke the function immediately (it just returns a new function that you can call later)._

  _Binding **this** :_

  _```const person = {```_\
  _``` name : "Alice",```_\
  _``` greet() {```_\
  _```  console.log(`Hi, i'm ${this.name}`);```_\
  _``` }```_\
  _```};```_

  _```const greetFunc = person.greet;```_\
  _```greetFunc();``` X : Undefined, because 'this' is lost._

  _```const boundGreet = person.greet.bind(person);```_\
  _```boundGreet();``` output : "Hi, i'm Alice"_

  _Pre-Filling Arguments :_

  _```function multiply(a, b) {```_\
  _``` return a * b;```_\
  _```}```_

  _```const double = multiply.bind(null, 2);``` Pre-fill a = 2_\
  _```console.log(double(5));``` output : 10_

  <sub>double is a new function where ```a``` is always 2, so calling ```double(5)``` runs ```multiply(2, 5)```.<sub>

  _Once a function is bound, is not possible to re-bind it (the first binding is permanent)._
  
* _**toString()** : this method is available on all JS objects, it is indeed defined on **Object.prototype**, but **functions override it** with their own version provided by **Function.prototype**. When called on a function, **.toString()** returns the source code of the function as a string._
* _**name** (property) : returns the **name** of the function._
* _**length** (property) : returns the **number of parameters** the function is declared with._
  
## _Hoisting_

_In JavaScript, **hoisting** is a behavior where declarations of variables and functions are conceptually moved to the top of their containing scope during the compilation phase. This means that sometimes it's possible to use variables or call functions before their actual line of declaration appears in the source code. However, the exact behavior depends on the type of declaration involved :_

* _**Variables declared with var** : these variables have their declaration hoisted to the top of their scope, meaning JavaScript knows the variable exists even before the line where it is written. However, the assignment (the actual value given to the variable) stays where it appears in the code. Because of this, trying to access the variable before the assignment line does not cause an error, but the variable's value will be **undefined**._
  
* _**Variables declared with let and const** : these variables are **hoisted** as well, but they are **not initialized** immediately. Instead, they are hoisted into a **temporal dead zone** (**TDZ**), which is the period between entering their block scope and the variable's actual declaration. During this time, accessing these variables results in a **ReferenceError**._ 

* _**Function Declarations** are hoisted entirely (name and definition) so they can be called before they appear in the code :_

  _```greet();```_\
  _```function greet() {```_\
  _```  console.log("Hello");```_\
  _```}```_

* _**Function expressions** and **Arrow functions** are not hoisted with their definition. Only the variable declaration is hoisted (as **undefined**), so calling them before the assignment causes an error._

  _```greet();```_\
  _```const greet = function() {```_\
  _```  console.log("Hello");```_\
  _```};```_

_<sub>TypeError : greet is not a function.<sub>_

## _Scope and Closures_

_**Scope** in JavaScript is the current context of execution. It determines which variables are accessible at a given part of the code._

 * _**Global Scope** : Variables declared **outside** any function or block are called **global** and are accessible anywhere in the code after declaration._

    _```let globalVar = "i'm global";```_
   
    _```function show() {```_\
    _``` console.log(globalVar);```_\
    _```}```_

   _```show();```_\
   _```console.log(globalVar);```_

   _<sub>globalVar is accessible from **anywhere**.<sub>_
   
 * _**Function Scope** : Variables declared with **var**, **let**, or **const** inside a function are accessible only within that function._

   _```function example() {```_\
   _``` let localVar = "Inside function";```_\
   _``` console.log(localVar);```_\
   _```}```_

   _```example();```_
   
   _```console.log(localVar);```_ ***ReferenceError***

   _<sub>The variable is accessible only inside the function where is declared so we'll get a **ReferenceError** trying to log it outside the function.<sub>_
   
 * _**Block Scope** : Applies to **let** and **const** inside blocks {}. These variables are accessible only inside the block._

   _```if (true){```_\
   _``` let blockVar = "Inside block";```_\
   _``` console.log(blockVar);```_\
   _```}```_

   _```console.log(blockVar)```_ ***ReferenceError***

   _<sub>var does not respect block scope. It is **function-scoped** or **global**.<sub>_
   
 * _**Lexical Scope** : also called **static scope** means that a function can access variables from the scope where it was **defined**, not where it is called._

   _```function outer(){```_\
   _``` let outerVar = "i'm from outer scope";```_

   _``` function inner(){```_\
   _```  console.log(outerVar);```_\
   _```  }```_

   _``` inner();```_\
   _```}```_

   _```outer();```_

   _<sub>inner has access to outerVar because it's defined inside outer, and that's its lexical environment<sub>_

_A **Closure** is when a function remembers and can use variables from the place where it was created, even after that outer function has finished running. This is possible because functions in JavaScript **retain a reference** to their lexical environment._

 _```function makeCounter(){```_\
 _``` let count = 0;```_

 _``` return function(){```_\
 _```  count++;```_\
 _```  return count;```_\
 _``` };```_\
 _```}```_

 _```const counter1 = makeCounter();```_\
 _```console.log(counter1());```_ ***1***\
 _```console.log(counter1());```_ ***2***

 _```const counter2 = makeCounter();```_\
 _```console.log(counter2());```_ ***1***

 _<sub>Each call to makeCounter() creates a new closure with its own count variable<sub>_

## _this Keyword_

_In JavaScript, **this** is a special keyword that refers to the context in which a function is executed. The value of **this** depends on how a function is called, not where it's defined. It can refer to different things depending on the situation :_

  * _**Global Context** : in the global scope (outside of any function), **this** refers to the **global object**;_
  * _**Inside a Regular Function** : **this** refers to the **global object** (in non-strict mode), or **undefined** (in strict mode);_
  * _**Inside an Object Method** : when a function is called as a method of an object, **this** refers to the **object itself**;_

    _```const person = {```_\
      _```name: "Alice",```_\
      _```greet() {```_\
        _```console.log("Hi, I'm " + this.name);```_\
      _```}```_\
    _```};```_

    _```person.greet();```_

  _<sub>The output will be "Hi, i'm Alice".<sub>_
    
  * _**Arrow Functions** : do not have their own **this**. They inherit **this** from the surrounding (lexical) scope;_

    _```const person = {```_\
      _```name: "Bob",```_\
      _```greet: () => {```_\
        _```console.log("Hi, I'm " + this.name);```_\
      _```}```_\
    _```};```_

    _```person.greet();```_

  _<sub>The output will be "Hi, i'm undefined" because objects do not create their own **lexical environment** (only functions and blocks do). Therefore, the arrow function inherits the value of **this** from the surrounding scope, which is not the object itself.<sub>_

  * _**Constructor Functions** : when a function is used with **new**, **this** refers to the new object being created._

    _```function Animal(name) {```_\
      _```this.name = name;```_\
    _```}```_

    _```const dog = new Animal("Fido");```_\
    _```console.log(dog.name);```_

    _<sub>The output will be "Fido"<sub>_

## _Objects_

_An object is a data structure that represents a complex entity made up of a collection of **properties** and **methods**. Properties are values associated with names (also called keys), while methods are functions attached to the object._\
_In other words, an object groups together heterogeneous data (such as strings, numbers, arrays, other objects) and related functionality into a single entity with its own identity._\
_Typically, objects are used to model real-world or abstract things like a person, an order or even more technical concepts._

_In JS, objects are **dynamic by nature**, meaning it's possible to add new properties at any time simply by assigning them using dot notation or bracket notation. There's no need to predefine all properties when the object is created._

_```const person = {};```_\
_```person.name = "Alice";```_\
_```person["city"] = "London";```_

### _Properties (Data)_

_An object's properties are **name-value pairs**, where the name is a string (the key) and the value can be any data type._

 _```const person = {```_\
 _``` name : "Simon",```_\
 _``` age : 20,```_\
 _``` city : "Rome"```_\
 _```};```_

_<sub>Here, name, age, and city are **properties**.<sub>_

### _Methods (Functionality)_

_A method is a function associated with an object. Methods define behaviors or actions that the object can perform or that operate on the object's data._

_```const person = {```_\
_``` name : "Simon",```_\
_``` age : 20,```_\
_``` greet : function() {```_\
_```  console.log("Hello, my name is " + this.name);```_\
_``` }```_\
_```};```_

_```person.greet();``` Output : Hello, my name is Simon._

_<sub>Here, greet is a **method** (a function defined as a property of the person object). The keyword **this** refers to the object itself.<sub>_

### _Create Objects_

_JS offers several ways to create objects :_

 * _**Object Literal Syntax** : the simplest and most common way to create an object. An object is defined directly with curly braces **{}**, specifying **key-value pairs** inside._

   _```const person = {```_\
   _``` name : "Simon",```_\
   _``` age : 20,```_\
   _``` greet : function() {```_\
   _```  console.log("Hi, i'm " + this.name);```_\
   _``` }```_\
   _```};```_

   _After creating the object it's possible to access or modify properties and call methods._

   _```console.log(person.name);``` output : Simon_\
   _```person.age = 21;``` modify the age property_\
   _```person.greet();``` output : Hi, i'm Simon_

   _It's also possible to create an empty object and then populate it :_

   _```const person = {};```_\
   _```person.firstName = "Mario";```_\
   _```person.lastName = "Rossi";```_

* _**new Object()** : In JS, **Object** is a **function** (specifically, a constructor function) used to create plain objects. The objects it creates, like all objects in JS, inherit from **Object.prototype**, which makes **Object** the base of almost all structures in the language._

  _```const car = new Object();```_\
  _```car.make = "Toyota";```_\
  _```car.model = "Corolla";```_\
  _```car.year = 2020;```_\
  _```car.getInfo = function() {```_\
  _``` return this.make + " " + this.model + " (" + this.year + ")";```_\
  _```};```_

  _```console.log(car.getInfo());``` output : Toyota Corolla (2020)_

* _**Costructor Functions** : used to create multiple objects with the same structure._

  _```function Person(name, age) {```_\
  _``` this.name = name;```_\
  _``` this.age = age;```_\
  _``` this.greet = function() {```_\
  _```  console.log("Hello, my name is " + this.name);```_\
  _``` };```_\
  _```}```_

  _```const person1 = new Person("Bob", 25);```_\
  _```const person2 = new Person("Carol", 24);```_

  _```person1.greet();``` output : Hello, my name is Bob._\
  _```person2.greet();``` output : Hello, my name is Carol._

  _<sub>Using **new** with the constructor function creates a new object where **this** refers to the new instance.<sub>_
  
* _**ES6 Classes** : introduced in **ES6** (**ECMAScript 2015**), classes provide a clearer, more concise syntax for creating objects with shared properties and methods._

  _```class Person {```_\
  _``` constructor(name, age) {```_\
  _```  this.name = name;```_\
  _```  this.age = age;```_\
  _``` }```_

  _``` greet() {```_\
  _```  console.log(`Hi, i'm ${this.name}`);```_\
  _``` }```_\
  _```}```_

  _```const person1 = new Person("Anna", 30);```_\
  _```person1.greet();```_

  _A class is a blueprint for creating objects where the constructor method automatically initializes properties, and methods can be defined cleanly without repeating the **function** keyword._

 _<sub>Using **new** with a class creates a new instance. The constructor sets initial properties, and class methods are shared via the prototype.<sub>_

### Shared Methods in All Objects

_All JavaScript objects inherit from **Object.prototype** by default. This inheritance provides a set of core methods that are available on all standard objects :_

* _```toString()``` : returns a string representation of the object. Automatically called when the object is used in a string context._

  _```const obj = {};```_\
  _```console.log(obj.toString());``` output : "[Object Object]"_

  _**Custom override**_

  _```const user = {```_\
  _``` name : "Leo",```_\
  _``` toString() {```_\
  _```  return `User : ${this.name}`;```_\
  _``` }```_\
  _```};```_\
  _```console.log(user.toString());``` output : "User : Leo"_

  _**Array behavior**_

  _For arrays, ```toString()``` returns a comma-separated string of elements._

  _<sub>Internally, arrays override the default ```toString()``` with their own implementation.<sub>_

* _```valueOf()``` : returns the primitive value of the object. Automatically called during numeric operations, comparisons, or type coercion._

  _Useful to customize how an object behaves when used in arithmetic or comparison contexts._

  _```const amount = {```_\
  _``` value : 100,```_\
  _``` valueOf() {```_\
  _```  return this.value;```_\
  _``` }```_\
  _```};```_

  _<sub>By default, objects return themselves. Custom implementation is required to convert objects to primitive values.<sub>_

* _```hasOwnProperty(prop)``` : checks if the specified property exists directly on the object itself, excluding properties inherited through the prototype chain._

  _```const obj = {a : 1};```_\
  _```console.log(obj.hasOwnProperty("a"));``` output : true_
  _```console.log(obj.hasOwnProperty("toString"));``` output : false_

* _```isPrototypeOf(obj)``` : indicates whether the current object exists in the prototype chain of another object._

  _```function Animal() {}```_\
  _```const dog = new Animal();```_

  _```console.log(Animal.prototype.isPrototypeOf(dog));``` output : true_

* _```propertyIsEnumerable(prop)``` : checks if a property is a direct property of the object and if it is enumerable/iterable (visible in **for...in** loops or **Object.keys**)._

  _```const obj = {a : 1};```_\
  _```console.log(obj.propertyIsEnumerable("a"));``` output : true_\
  _```console.log(obj.propertyIsEnumerable("toString"));``` output : false_
  
* _```constructor``` : references the function (or class) used to construct the object instance. It is automatically set on every object created via a constructor function or class, and points to the original constructor that created the instance._

  _```function Car(make, model) {```_\
  _``` this.make = make;```_\
  _``` this.model = model;```_\
  _```}```_

  _```const myCar = new Car("Toyota", "Corolla");```_

  _```console.log(myCar.constructor === Car );``` output : true_

## _Autoboxing_

_JavaScript provides built-in object types that correspond to primitive data types :_

 * **String**
 * **Number**
 * **Boolean**
   
_Autoboxing is the automatic process by which JavaScript wraps primitive values (like strings, numbers, and booleans) into their corresponding object types when a method or a property is accessed._

_Even though primitive values are **not objects**, JS allows them to behave like objects temporarily by internally wrapping them with a constructor object (```String```, ```Number```, or ```Boolean```)._

_```const message = "hello";```_\
_```console.log(message.length);``` output : 5_\
_```console.log(message.toUpperCase());``` output : "HELLO"_\

_Behind the scenes, JS internally creates a temporary **String** object wrapper, calls the method, and then discards it :_

_```new String("hello").length;```_\
_```new String("hello").toUpperCase();```_

_<sub>The original primitive remains unchanged.<sub>_

## _new Keyword_

_The new keyword is used to create a new object instance from a constructor function or a class. It automates several steps behind the scenes to correctly set up the new object :_

* _Creates an empty object;_
* _Sets up the prototype chain : sets **[[Prototype]]** of the new object to the constructor's ```.prototype```._
* _Binds **this** to the new object inside the constructor function;_
* _Returns the newly created object (unless the constructor explicitly returns a different object)._

_```function Person(name) {```_\
_``` this.name = name;```_\
_```}```_

_```const p = new Person("Alice");```_\
_```console.log(p.name);```_

_<sub>Without **new**, the constructor function behaves like a regular function, and **this** will refer to the global object (**window** in browsers) or **undefined** in strict mode.<sub>_

## _Spread Syntax (...)_

_The **spread syntax** is represented by three dots and is used to expand ("spread") the elements of an iterable object (such as an array, string, or Set) into individual elements._

* Copying Arrays :

  _```const original = [1, 2, 3];```_\
  _```const copy = [...original];```_\
  _```console.log(copy);``` output : {1, 2, 3}_

* Merging Arrays :

  _```const arr1 = [1, 2];```_\
  _```const arr2 = [3, 4];```_\
  _```const merged = [...arr1, ...arr2];```_\
  _```console.log(merged);``` output : {1, 2, 3, 4}_

* Passing Array elements as function arguments :

  _```function sum(a, b, c){```_\
  _``` return a + b + c;```_\
  _```}```_\
  _```const numbers = [1, 2, 3];```_\
  _```console.log(sum(...numbers));```_

* Converting iterable to Array :

  _```const set = new Set([1, 2, 3]);```_\
  _```const array = [...set];```_\
  _```console.log(array);``` output : {1, 2, 3}_

_<sub>Using the spread syntax avoids reference sharing and creates a new structure, ensuring values are passed by value (for primitive) rather than by reference (for arrays or objects).<sub>_

_<sub>The spread syntax works only on iterable values and produces a **shallow copy**, meaning that nested structures (like arrays or objects within the array) are copied by reference, not cloned.<sub>_

## _Prototype Chain and Inheritance_

_In JavaScript, **inheritance** is primarily achieved through the **prototype chain**. Every object in JS has an internal link called **[[Prototype]]**, which references another object known as its **prototype**, this link between objects forms what is known as the **prototype chain**._

_In JS, every function (when not an arrow function) has a special property called ```.prototype```. This property is automatically created by the language when the function is defined._

_When a function is used as a **constructor** (with the ```new``` keyword), its ```.prototype``` becomes the **[[Prototype]]** of the objects it creates._

 _```function Animal(name) {```_\
 _``` this.name = name;```_\
 _```}```_

_<sub>```Animal``` is a **constructor** function.<sub>_

_<sub>**Animal.prototype** is an object that will be assigned as the **[[Prototype]]** of any object created using ```new Animal()```.<sub>_

_```const dog = new Animal("Rex");```_\
_```console.log(Object.getPrototypeOf(dog) === Animal.prototype);``` output : true_

_<sub>By default, **Animal.prototype** is an empty object that inherits from **Object.prototype**. It's possible to add shared methods or properties to it.<sub>_

_```Animal.prototype.speak = function() {```_\
_``` console.log(this.name + " makes a noise.");```_\
_```};```_

_```dog.speak();``` output : "Rex makes a noise."_

_When a property or method is accessed on an object, JS first looks for it on the object itself. If it's not found, the engine traverses up the prototype chain, checking each linked prototype until it either finds the property or reaches the end of the chain._

_The **prototype chain** always ends with ```null```, which means there are no further prototypes to follow. At the top of the chain is usually ```Object.prototype```, whose own prototype is ```null```. Once ```null``` is reached, JS stops searching, and the property is considered **undefined** if not found earlier in the chain._

_This approach differs from classical inheritance models found in languages like Java or C++, where classes are the primary unit of inheritance. In JS, inheritance is **object-based**, meaning that objects inherit directly from other objects through this dynamic prototype mechanism._

## _Built-in Advanced Data Structures_

_In addition to basic objects and arrays, JavaScript provides built-in **advanced data structures** that offer more flexibility, performance, and precision in certain scenarios._

### _Map_

_A **Map** is a collection of **ordered** key-value pairs where **keys can be of any type**, including objects, functions, and primitives. It is more versatile than plain objects, especially when key types other than strings are required._

_```const myMap = new Map();```_\
_```myMap.set("name", "Alice");```_\
_```myMap.set(42, "Quit");```_

_```const key = {id : 1};```_\
_```myMap.set(key, "Object key");```_

_<sub>All three, ```name```, ```42``` and ```key``` are **keys**, and they are of different types.<sub>_

_A Map preserves the insertion order of entries, accepts keys of any type (including objects and functions, unlike plain objects that coerce keys to strings), and provides a clean, consistent API with methods like ```.set()``` and ```.get()``` for intuitive and powerful data management._

_Common Map methods/properties are :_

* _```set(key, value)``` : adds or updates an entry._
* _```get(key)``` : retrieves the value for the given key._
* _```has(key)``` : checks if a key exists._
* _```delete(key)``` : removes the entry for the given key._
* _```clear()``` : removes all entries._
* _```size``` : returns the number of entries._

_Each entry in a **Map** is structured as a two-element array, consisting of the key and its corresponding value._\
_One of the most common ways to iterate through a **Map** is by using a **for...of** loop combined with destructuring. This approach allows direct access to both the key and the value in each iteration._

_```const myMap = new Map();```_\
_```myMap.set("fruit", "apple");```_\
_```myMap.set("color", "red");```_

_```for (const [key, value] of myMap) {```_\
_``` console.log(`${key} => ${value}`);```_\
_```}```_

_**Map** also provides dedicated methods for targeting specific elements. The ```.keys()``` method allows iteration over just the keys, while ```.values()``` returns only the values. The ```.entries()``` method gives access to key-value pairs and is the default iterator for a **Map**._

_```for (const key of myMap.keys()) {```_\
_``` console.log(key);```_\
_```}```_

_<sub>Will output all the keys<sub>_

_```for (const value of myMap.values()) {```_\
_``` console.log(value);```_\
_```}```_

_<sub>Will output all the values<sub>_

### _Set_

_A **Set** is a built-in object, it represents a collection of unique values, meaning each element can appear only one in the structure. Duplicate entries are automatically excluded._

_```const set1 = new Set();```_

_```const set2 = new Set([1, 2, 3, 3]);```_\
_```console.log(set2);``` output : {1, 2, 3}_

_A **Set** mantains insertion order and accepts values of any data type._

_Common Set methods/properties are :_

* _```add(value)``` : adds a value to the set._
* _```delete(value)``` : removes a value from the set._
* _```has(value)``` : checks if a value exists in the set._
* _```clear()``` : removes all values._
* _```size``` : returns the number of unique values in the set._

_The most common way to iterate over a Set are :_

* _with the **for...of** loop :_
  
 _```const colors = new Set(["red", "green", "blue"]);```_

 _```for (const color of colors){```_\
 _``` console.log(color);```_\
 _```}```_

 _```colors.forEach(color => console.log(color));```_

* _with forEach() :_

 _```const colors = new Set(["red", "green", "blue"]);```_\
 _```colors.forEach(color => console.log(color));```_

_It's very easy to convert between Set and Array :_

* _Set to Array :_

   _```const set = new Set([1, 2, 3]);```_\
   _```const array = [...set];```_

* _Array to Set (removes duplicates) :_

  _```const numbers = [1, 2, 2, 3];```_\
  _```const uniqueNumbers = [...new Set(numbers)];```_\
  _```console.log(uniqueNumbers);``` output : {1, 2, 3}_

## _Custom Advanced Data Structures_

_These structures are built manually to match particular algorithmic or architectural needs :_

* ***Stack***
* ***Queue***
* ***Linked List***
* ***Tree***
* ***Graph***
* ***Heap***
* ***Trie (Prefix Tree)***
