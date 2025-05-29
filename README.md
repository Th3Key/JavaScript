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

#### _Code Blocks_

_A code block is a group of one or more statements enclosed within curly braces ```{ }```. It allows multiple statements to be treated as a single unit, meaning all the code inside the braces is executed together as a block. Code blocks help **organize** code logically and improve **readability** and **maintainability** by clearly grouping related instructions._

#### _Conditional Statements_




