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

## _Data Types_

_Data types define the kind of value a variable can hold. JavaScript is a **dynamically typed language**, meaning you don't need to declare the type of a variable (it is determined automatically at runtime)._\
_Despite being flexible, JS still enforces rules based on the type of the data we are working with (these rules affect how values behave, how operations are performed and how values are compared)._

_JavaScript data types are divided into two main categories :_

* _**Primitive Types** :_
  
  _**Basic**, **immutable** values (once a primitive value is created, it cannot be altered; however, the variable holding it can be reassigned to a new value). These values are stored directly in memory and **compared by value**, not by reference._
  
    _- ```string```: a **sequence of characters** delimited by double or single quotes (it is possible to insert special characters inside a string by using the escaping character ```\``` )._
  
    _- ```number```: includes both **whole numbers** and **decimals**; in addition to the classic base ten notation, we can represent numbers in **octal** (the number starts with ```0```) and **hexadecimal** notation (the number starts with ```0x```). Any value that goes outside the representable range does not generate an exception but is represented by two special values : **Infinity** and **-Infinity**._\
  
  _<sub>Another special numeric value is **NaN** (Not a Number) which indicates an undefined numeric value.<sub>_
  
  _- ```bigint```: used for very **large integers**, beyond the number limit._\
  _- ```boolean```: **True** or **False** values._\
  _- ```undefined```: a variable that has been declared but not given a value._\
  _- ```null```: rapresents an intentional **empty value**._\
  _- ```symbol```: creates a unique, unchangeable value, used ad object property keys._
  
* _**Non-Primitive Types** (Objects) :_
  
  _Complex types like **arrays**, **functions** and **objects** (**mutable** and stored **by reference**)._

## _Variables_

_A variable is a container that holds a value. There are three main ways to declare variables in JS :_

* _```let```: for variables that can change. It is **block-scoped** (exists only inside the {} block where they are defined)._
* _```const```: for variables that must not change. It is **block-scoped**._
* _```var```: the old way (avoid using it). It is **function-scoped** (exists in the whole function)._

_Variables declared with **var** are **hoisted** (moved to the top of their scope) and initialized to **undefined**, while variables declared with **let** and **const** are **hoisted** too, but **not initialized**. This is because **let** and **const** are hoisted into a **temporal dead zone** (**TDZ**), which is the space between entering the block and the variable's actual declaration (where the variable exists but cannot be accessed)._

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
  _<sub>**key** represents each property name (as a string) on the object.<sub>_\

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

### Return Statement

_The **return** statement is used in functions to send a value back to the place where the function was called. When a function reaches a return statement, it stops executing and returns the specified value._\
_Without a return statement, a function returns **undefined** by default._

_```function multiply(a, b){```_\
_```  return a * b;```_\
_```}```_

_```const result = multiply(4, 5);```_\
_```console.log(result);```_

<sub>The multiply function calculates the product of two numbers and returns the result. The returned value is then stored in the variable result and printed to the console.<sub>
