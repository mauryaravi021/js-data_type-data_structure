# JavaScript data types and data structures
## Dynamic typing
---

JavaScript is a loosely typed and dynamic language. Variables in JavaScript are not directly associated with any particular value type, and any variable can be assigned (and re-assigned) values of all types:

```javascript
let foo = 42;    // foo is now a number
foo     = 'bar'; // foo is now a string
foo     = true;  // foo is now a boolean
```
JavaScript provides different data types to hold different types of values. There are two types of data types in JavaScript.

1. Primitive data type
2. Non-primitive (reference) data type

## Primitive data type
---
All types except objects define immutable values (that is, values which can't be changed). For example (and unlike in C), Strings are immutable. We refer to values of these types as "primitive values".<br><br>
There are five types of primitive data types in JavaScript. They are as follows:

> Boolean type :

&nbsp; &nbsp;&nbsp;Boolean represents a logical entity and can have two values: true and false.

```javascript
var x = 5;
var y = 5;
var z = 6;
(x == y)       // Returns true
(x == z)       // Returns false 
```
> Null type :

&nbsp; &nbsp;&nbsp;The Null type has exactly one value: null.

```javascript
var myVar = null;

alert(myVar); // null 

```

> Undefined type :

&nbsp; &nbsp;&nbsp;A variable that has not been assigned a value has the value undefined.

```javascript
var myVar;

alert(myVar); // undefined 

```

> Number type :

&nbsp; &nbsp;&nbsp;JavaScript has only one type of numbers. Numbers can be written with, or without decimals:

```javascript
var x1 = 34.00;     // Written with decimals
var x2 = 34;        // Written without decimals 
```

> String type :

&nbsp; &nbsp;&nbsp;String is a primitive data type in JavaScript. A string is textual content. It must be enclosed in single or double quotation marks. 

```javascript
var str1 = "Hello World";

var str2 = 'Hello World';
```

> Symbol type :

&nbsp; &nbsp;&nbsp; A Symbol is a unique and immutable primitive value and may be used as the key of an Object property. In some programming languages, Symbols are called "atoms".

```javascript
var object1 = {
   name: ‘Shalini’,
   age: 25,
   city: ‘Mumbai’
}
var occupation=Symbol(‘engineer’);

	
typeof(occupation);  // returns symbol
```
<br><br>
## Non-primitive (reference) data type
---
The ‘object’ is a non-primitive data type in JavaScript. Arrays and Functions in JavaScript belong to the ‘object’ data type.

> Object:

&nbsp; &nbsp; &nbsp; An object in JavaScript contains key-value pairs in its address. When we refer to obj1, we are actually referring to the address in memory which contains the value {a: 5, b: 6}, instead of the value {a: 5, b: 6} directly.

```javascript
var obj1 = { a: 5, b: 6 };

typeof (obj1) // will return the data type ‘object’.
```

> Array :

&nbsp; &nbsp; &nbsp; An array in JavaScript is an object data type. An array contains more than one value with a numerical index, where the index starts from 0. Thus it holds its value in a key-value pair.

```javascript
var arr1= [1, 2, 3];

typeof (arr1) // will return the data type ‘object’
```
> Function :

&nbsp; &nbsp; &nbsp; A JavaScript function is a block of code designed to perform a particular task.

&nbsp; &nbsp; &nbsp; A JavaScript function is executed when "something" invokes it (calls it).

```javascript
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}
```
<br><br><br><br>

## Data Structure in javascript
---

JavaScript has built in support for the following data structures:
1. Array
2. Set
3. Map
<br><br>

> ### Array 

&nbsp; &nbsp;&nbsp;JavaScript arrays are used to store multiple values in a single variable and can be accessed the values by referring index number.

Example -

```javascript
var cars = ["Saab", "Volvo", "BMW"];
```

Syntax :

```javascript
var array_name = [item1, item2, ...];  
```

### Some methods in array

    push( ) :

This method adds one or more elements to the end of array and returns the new length of the array.

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.push("Kiwi");       //  Adds a new element ("Kiwi") to fruits 
```
    splice() :

The splice() method can be used to add new items to an array: 

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.splice(2, 0, "Lemon", "Kiwi");  // Banana,Orange,Lemon,Kiwi,Apple,Mango
```

    slice() :

The slice() method slices out a piece of an array into a new array.

This example slices out a part of an array starting from array element 1 ("Orange"):

```javascript
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];

var citrus = fruits.slice(1); // Orange,Lemon,Apple,Mango
``` 

* some more method :
~~~
* map( )
* filter( )
* sort( )
* forEach( )
* concat( )
* every( )
* some( )
* includes( )
* join( )
* reduce( )
* find( )
* findIndex( )
* indexOf( )
* fill( )
* slice( )
* reverse( )
* push( )
* pop( ) 
~~~ 
<br><br>
> Set :

The Set object lets you store unique values of any type, whether primitive values or object references.<br>
Set objects are collections of values. You can iterate through the elements of a set in insertion order. A value in the Set may only occur once; it is unique in the Set's collection.

Syntax :

```javascript
Set(); //Creates a new Set object. 
```
> Instance methods present in set :


    Set.prototype.add(value)

Appends value to the Set object. Returns the Set object with added value.

    Set.prototype.clear()

Removes all elements from the Set object.

    Set.prototype.delete(value)

Removes the element associated to the value and returns a boolean asserting whether an element was successfully removed or not. Set.prototype.has(value) will return false afterwards.

    Set.prototype.has(value)

Returns a boolean asserting whether an element is present with the given value in the Set object or not. 

Example --

```javascript
// ["sumit","amit","anil","anish"] 
var set1 = new Set(["sumit","sumit","amit","anil","anish"]); 
  
// it contains 'f', 'o', 'd' 
var set2 = new Set("fooooooood"); 
  
// it contains [10, 20, 30, 40] 
var set3 = new Set([10, 20, 30, 30, 40, 40]); 
  
 // it is an  empty set 
var set4 = new Set(); 
```
<br><br>

> Map :

Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.

Syntax :

```javascript
new Map(); ///creates the map.
```
<br>

> Methods and properties are:

<br>

    map.set(key, value)

 stores the value by the key.

    map.get(key)

 returns the value by the key, undefined if key doesn’t exist in map.

    map.has(key)

 returns true if the key exists, false otherwise.

    map.delete(key)

 removes the value by the key.

    map.clear()

 removes everything from the map.

    map.size

 returns the current element count.

 Example --

```javascript
let map = new Map();

map.set('1', 'str1');   // a string key
map.set(1, 'num1');     // a numeric key
map.set(true, 'bool1'); // a boolean key

// remember the regular Object? it would convert keys to string
// Map keeps the type, so these two are different:
alert( map.get(1)   ); // 'num1'
alert( map.get('1') ); // 'str1'

alert( map.size ); // 3
```