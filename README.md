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

* #### _Primitive Types :_
  _**Basic**, **immutable** values (once a primitive value is created, it cannot be altered; however, the variable holding it can be reassigned to a new value). These values are stored directly in memory and **compared by value**, not by reference._
  
  _- ```string```: a **sequence of characters** delimited by double or single quotes (it is possible to insert special characters inside a string by using the escaping character ```\``` )._
  
  _- ```number```: includes both **whole numbers** and **decimals**; in addition to the classic base ten notation, we can represent numbers in **octal** (the number starts with ```0```) and **hexadecimal** notation (the number starts with ```0x```). Any value that goes outside the representable range does not generate an exception but is represented by two special values : **Infinity** and **-Infinity**._\
  
  _Another special numeric value is **NaN** (Not a Number) which indicates an undefined numeric value._
  
  _- ```bigint```: used for very **large integers**, beyond the number limit._\
  _- ```boolean```: **True** or **False** values._\
  _- ```undefined```: a variable that has been declared but not given a value._\
  _- ```null```: rapresents an intentional **empty value**._\
  _- ```symbol```: creates a unique, unchangeable value, used ad object property keys._
* #### _Non-Primitive Types (Objects) :_
  _Complex types like **arrays**, **functions** and **objects** (**mutable** and stored **by reference**)._
