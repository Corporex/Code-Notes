# JavaScript-[Array-JS](-Array-JavaScript)
_Source: Array JavaScript - Udacity Front End Web Development Nanodegree_


### Table Of Contents:
- a. __What is an Array?__
- b. __Create an Array__
- c. __Store different types of data__
- d. __Array Properties and Methods__
- e. __Property: .length__ 
- f. __push() method__ 
- g. __pop() method__
- h. __slice/splice() method__
- i. __Array Loops__
- j. __For Loop__

### a. What is an Array?
- An __array__ `[]` = _ordered collection of elements, enclosed by square brackets []._
- It is one of the most useful data structures in JavaScript, as it stores __multiple values into a single, organized data structure.__ 

### b. Create an Array
- Define a new array by _listing values_ _separated with commas_ `,` between _square brackets_ `[]`.
- __Example:__  variable "myArray", assigned to an empty array:
```
const myArray = [];
```
- Each element in an array is referenced by a __numeric key__ (`index`).
- It starts from zero and increments by one for each additional element in the array. 
- __Example:__ 
```
const fruits = ['apple', 'banana', 'orange', 'grape', 'lychee'];
console.log(fruits);
```
// ['apple', 'banana', 'orange', 'grape', `lychee`]

- To access the __first (left-most) element__ in "fruits", access that element by its `index`:
```
fruits[0];
```
//= 'apple'
- To access the __last (right-most) element__ in "fruits",use its `index`:
```
fruits[4];
```
//= 'lychee'

### c. Store different types of data
- Arrays[] can store __different types of data__, not only strings!

// Create a `donuts` array with three strings
  * __A `string`__
```
var donuts = ["glazed", "powdered", "jelly"];
```  
// Create a `mixedData` array with mixed data types
  * __A `number`__
  * __A `boolean`__
```
var mixedData = ["abcd", 1, true, undefined, null, "all the things"];
```
// Create a `arraysInArrays` array with three arrays:
  * __Another array `nested array`__: store an array in an array to create a `nested array`
```
var arraysInArrays = [[1, 2, 3], ["Julia", "James"], [true, false, true, false]];
```
- Nested arrays can be hard to read. So, write them on one line, using a newline after each comma:
```
var arraysInArrays = [
  [1, 2, 3], 
  ["Julia", "James"], 
  [true, false, true, false]
];
```
### d. __Array Properties and Methods__
built-in methods

### e. __Array Property: .length__ (=to find length of an array)
- Find the __length of an array__ by using its length property. `.lenght`
- To access the length property, type the name of the array, followed by a period .
- The length property will then return the number of elements in the array.
```
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts.length);
```
__TIP:__ Strings have a length property too! Use it to get the length of any string. 
Example
```
"supercalifragilisticexpialidocious".length 
```
returns 34.

### f. __push() method__ (=to "add" elements to the end of an array.)
- The two most common methods for __modifying an array__ are 
  1) `push()` to add an element to the end of an Array[] = `arr.push(element1[, ...[, elementN]])`
- __Example:__ _Represent the spread of donuts using an array_
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
```
// Push donuts onto the __end of the array__ using the push() method= pushes "powdered" onto the end of the `donuts` array
```
donuts.push("powdered"); 
```
// the `push()` method returns 7 because the `donuts` array now has 7 elements
Returns: 7
```
donuts array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"]
```
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
donuts.push("powdered"); 
```
__NOTE:__ 
  1) with the `push() method` you need to pass the value of the element you want to add to the end of the array. 
  2) The `push() method` returns the length of the array after an element has been added.

### g. __pop() method__ (=to "remove" elements from the end of an array) 
  2) `pop()` to remove an element from the end of an Array[] = `arr.pop()`
  - __Example:__
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"];
```
```
donuts.pop(); // pops "powdered" off the end of the `donuts` array
donuts.pop(); // pops "sprinkled" off the end of the `donuts` array
donuts.pop(); // pops "cinnamon sugar" off the end of the `donuts` array
```
Returns: "cinnamon sugar"
```
donuts array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"]
```
__NOTE:__ 
- With the pop() method there is __NO__ need to _pass a value_ 
- pop() will __always remove the last element from the end of the array.__ 
- pop() _returns the element that has been removed_ in case you need to use it.

```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"];
donuts.pop(); 
```
// the `pop()` method returns "powdered" because "powdered" was the last element on the end of `donuts` array
- Returns: "powdered"

### h. __Array: splice() method__: (to add and remove elements from _anywhere within_ an array).
- The `splice()` method = to `add and remove elements from anywhere within an array`.
- It specify the index location to add new elements
- It specify the number of elements to delete (if any).
- The __first argument__ represents the `starting index` from where to change the array
- The __second argument__ represents the `elements to remove`
- The __remaining arguments__ represent the `elements to add`.
- Using the splice() method adds and removes elements from any location in an array.
- splice() is an incredibly powerful method that allows you to manipulate your arrays in a variety of ways. 
- Any combination of adding or removing elements from an array can all be done in one simple line of code.
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"];
donuts.splice(1, 1, "chocolate cruller", "creme de leche"); 
```
// removes "chocolate frosted" at index 1 and adds "chocolate cruller" and "creme de leche" starting at index 1
Returns: ["chocolate frosted"]
```
donuts array: ["glazed", "chocolate cruller", "creme de leche", "Boston creme", "glazed cruller"]
```
- i. __Array Loops__
Use a `loop`= to _efficiently access and manipulate each element in the array without writing repetitive code for each element_.
```
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];
```
// Manually= make all the same donut types, but only sell them as donut holes instead
```
donuts[0] += " hole";
donuts[1] += " hole";
donuts[2] += " hole";
donuts array: ["jelly donut hole", "chocolate donut hole", "glazed donut hole"]
```
//or `Loop through an array`
//use a variable to represent the index in the array, and loop over that index to perform whatever manipulations desired.
```
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];
```
// the variable `i` is used to step through each element in the array
// As i is incremented, step over each element in the array starting from 0 until donuts.length - 1 (donuts.length is out of bounds).
``` 
for (var i = 0; i < donuts.length; i++) {
    donuts[i] += " hole";
    donuts[i] = donuts[i].toUpperCase();
}
donuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]
```
#### Resources 
- [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
- [Pop()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
- [Splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

#### Take Away
- An `array[]` = _ordered collection of elements, enclosed by []._
- It stores __multiple values into a single, organized data structure.__ 
- `push()`method add elements to the end of an array
- `pop()`method remove elements from the end of an array
- `splice()`method add and remove elements from anywhere within an array.

