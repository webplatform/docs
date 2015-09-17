---
title: 'core objects'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Predefined_Core_Objects)'
notes:
  - "Merge Candidate:  This page is a candidate for merge with the following pages: [[1]] \n\n\n\n\nSplit Candidate:   Currently this page handles all Core Objects. These should be split to seperate pages, with links to the individual pages from the javascript Objects page."
readiness: 'In Progress'
summary: 'This chapter describes the predefined objects in core JavaScript: Array, Boolean, Date, Function, Math, Number, RegExp, and String.'
tags:
  - Tutorials
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/programming/javascript/core objects/guides/js/Values'
    - 'concepts/programming/javascript/core objects/dom'
    - 'concepts/programming/javascript/core objects/js/objects/Array/forEach'
    - 'concepts/programming/javascript/core objects/js/objects/Array/concat'
    - 'concepts/programming/javascript/core objects/js/objects/Array/join'
    - 'concepts/programming/javascript/core objects/js/objects/Array/push'
    - 'concepts/programming/javascript/core objects/js/objects/Array/pop'
    - 'concepts/programming/javascript/core objects/js/objects/Array/shift'
    - 'concepts/programming/javascript/core objects/js/objects/Array/unshift'
    - 'concepts/programming/javascript/core objects/js/objects/Array/slice'
    - 'concepts/programming/javascript/core objects/js/objects/Array/splice'
    - 'concepts/programming/javascript/core objects/js/objects/Array/reverse'
    - 'concepts/programming/javascript/core objects/js/objects/Array/sort'
    - 'concepts/programming/javascript/core objects/js/objects/Array/indexOf'
    - 'concepts/programming/javascript/core objects/js/objects/Array/lastIndexOf'
    - 'concepts/programming/javascript/core objects/js/objects/Array/map'
    - 'concepts/programming/javascript/core objects/js/objects/Array/filter'
    - 'concepts/programming/javascript/core objects/js/objects/Array/every'
    - 'concepts/programming/javascript/core objects/js/objects/Array/some'
    - 'concepts/programming/javascript/core objects/js/objects/Array/Reduce'
    - 'concepts/programming/javascript/core objects/js/objects/Array/ReduceRight'
    - 'concepts/programming/javascript/core objects/js/objects/RegExp/exec'
    - 'concepts/programming/javascript/core objects/js/objects/String/match'
    - 'concepts/programming/javascript/core objects/js/objects/String/split'
    - 'concepts/programming/javascript/core objects/dom/NodeList'
    - 'concepts/programming/javascript/core objects/dom/document.getElementsByTagName'
    - 'concepts/programming/javascript/core objects/sj/functions/arguments'
    - 'concepts/programming/javascript/core objects/js/functions/arguments/length'
    - 'concepts/programming/javascript/core objects/guides/JavaScript/Iterators'
    - guides/JavaScript/Statements
    - 'concepts/programming/javascript/core objects/js/statements/function'
    - 'concepts/programming/javascript/core objects/js'
    - 'concepts/programming/javascript/core objects/js/objects/String/substring'
    - 'concepts/programming/javascript/core objects/js/objects/String/anchor'
    - 'concepts/programming/javascript/core objects/js/objects/String/big'
    - 'concepts/programming/javascript/core objects/js/objects/String/blink'
    - 'concepts/programming/javascript/core objects/js/objects/String/bold'
    - 'concepts/programming/javascript/core objects/js/objects/String/fixed'
    - 'concepts/programming/javascript/core objects/js/objects/String/italics'
    - 'concepts/programming/javascript/core objects/js/objects/String/small'
    - 'concepts/programming/javascript/core objects/js/objects/String/strike'
    - 'concepts/programming/javascript/core objects/js/objects/String/sub'
    - 'concepts/programming/javascript/core objects/js/objects/String/sup'
    - 'concepts/programming/javascript/core objects/js/objects/String/charAt'
    - 'concepts/programming/javascript/core objects/js/objects/String/charCodeAt'
    - 'concepts/programming/javascript/core objects/js/objects/String/indexOf'
    - 'concepts/programming/javascript/core objects/js/objects/String/lastIndexOf'
    - 'concepts/programming/javascript/core objects/js/objects/String/link'
    - 'concepts/programming/javascript/core objects/js/objects/String/fromCharCode'
    - 'concepts/programming/javascript/core objects/js/objects/String/slice'
    - 'concepts/programming/javascript/core objects/js/objects/String/replace'
    - 'concepts/programming/javascript/core objects/js/objects/String/search'
    - 'concepts/programming/javascript/core objects/guides/JavaScript/Working with Objects'
    - 'concepts/programming/javascript/core objects/guides/JavaScript/Details of the Object Model'
uri: 'concepts/programming/javascript/core objects'

---
## Summary

This chapter describes the predefined objects in core JavaScript: Array, Boolean, Date, Function, Math, Number, RegExp, and String.

## Array Object

JavaScript does not have an explicit array data type. However, you can use the predefined `Array` object and its methods to work with arrays in your applications. The `Array` object has methods for manipulating arrays in various ways, such as joining, reversing, and sorting them. It has a property for determining the array length and other properties for use with regular expressions.

An *array* is an ordered set of values that you refer to with a name and an index. For example, you could have an array called `emp` that contains employees' names indexed by their employee number. So `emp[1]` would be employee number one, `emp[2]` employee number two, and so on.

### Creating an Array

To create an `Array` object, the following three statements are equivalent:

``` js
var arr = new Array(element0, element1, ..., elementN);
var arr = Array(element0, element1, ..., elementN);
var arr = [element0, element1, ..., elementN];
```

`element0, element1, ..., elementN` is a list of values for the array's elements. When this form is specified, the array is initialized with the specified values as its elements, and the array's `length` property is set to the number of arguments.

The bracket syntax is called "array literal" or "array initializer". It is shorter and so is generally preferred. See [Array Literals](/w/index.php?title=concepts/programming/javascript/core_objects/guides/js/Values&action=edit&redlink=1) for details on array literals.

To create an Array with non-zero length, but without any items, either of the following can be used:

``` js
var arr = new Array(arrayLength);
var arr = Array(arrayLength);

 // This has exactly the same effect
var arr = [];
arr.length = arrayLength;
```

 Note: in the above code, `arrayLength` must be a `Number`. Otherwise, an array with a single element (the provided value) will be created. Calling `arr.length` will return `arrayLength`, but the array actually contains empty (undefined) elements. Running a for...in loop on the array will return none of the array's elements.

In addition to a newly defined variable as shown above, Arrays can also be assigned as a property of a new or an existing object:

``` js
var obj = {};
// ...
obj.prop = [element0, element1, ..., elementN];

// OR
var obj = {prop: [element0, element1, ...., elementN]}
```

 If you wish to initialize an array with a single element, and the element happens to be a `Number`, you must use the bracket syntax. When a single `Number` value is passed to the Array() constructor or function, it is interpreted as an `arrayLength`, not as a single element.

``` js
var arr = [42];
var arr = Array(42); // Creates an array with no element, but with arr.length set to 42

// The above code is equivalent to
var arr = [];
arr.length = 42;
```

 Furthermore, if you are creating an array with a single element, and the element happens to be a non-whole `Number` (a number with a non-trivial floating part), a `RangeError` is thrown. If there is a possibility that your code will be creating arrays with single elements, with arbitrary data type, it is safer to use array literals, or create an empty array first and then fill it up.

``` js
var arr = Array(9.3);  // RangeError: Invalid array length
```

### Populating an Array

You can populate an array by assigning values to its elements. For example:

``` js
var emp = [];
emp[0] = "Casey Jones";
emp[1] = "Phil Lesh";
emp[2] = "August West";
```

**Note:** if you supply a non-integer value to the array operator in the code above, a property will be created in the object representing the array, instead of an array element.

``` js
var arr = [];
arr[3.4] = "Oranges";
console.log(arr.length);                // 0
console.log(arr.hasOwnProperty[3.4]);   // true
```

 You can also populate an array when you create it:

``` js
var myArray = new Array("Hello", myVar, 3.14159);
var myArray = ["Mango", "Apple", "Orange"];
```

### Referring to Array Elements

You refer to an array's elements by using the element's ordinal number. For example, suppose you define the following array:

``` js
var myArray = ["Wind", "Rain", "Fire"];
```

 You then refer to the first element of the array as `myArray[0]` and the second element of the array as `myArray[1]`. The index of the elements begins with zero.

**Note**: The array operator (square brackets) is also used for accessing the array's properties (arrays are also objects in JavaScript). For example,

``` js
var arr = ["one", "two", "three"];
arr[2];  // three
arr["length"];  // 3
```

### Understanding length

At the implementation level, JavaScript's arrays actually store their elements as standard object properties, using the array index as the property name. The `length` property is special; it always returns the index of the last element. Remember, Javascript Array indexes are 0-based: they start at 0, not 1. This means that the `length` property will be one more than the highest index stored in the array:

``` js
var cats = [];
cats[30] = ['Dusty'];
print(cats.length); // 31
```

 You can also assign to the `length` property. Writing a value that is shorter than the number of stored items truncates the array; writing 0 empties it entirely:

``` js
var cats = ['Dusty', 'Misty', 'Twiggy'];
console.log(cats.length); // 3

cats.length = 2;
console.log(cats); // prints "Dusty,Misty" - Twiggy has been removed

cats.length = 0;
console.log(cats); // prints nothing; the cats array is empty

cats.length = 3;
console.log(cats);  // [undefined, undefined, undefined]
```

### Iterating over arrays

A common operation is to iterate over the values of an array, processing each one in some way. The simplest way to do this is as follows:

``` js
var colors = ['red', 'green', 'blue'];
for (var i = 0; i < colors.length; i++) {
  console.log(colors[i]);
}
```

 If you know that none of the elements in your array evaluate to `false` in a boolean context — if your array consists only of [DOM](/w/index.php?title=concepts/programming/javascript/core_objects/dom&action=edit&redlink=1) nodes for example, you can use a more efficient idiom:

``` js
var divs = document.getElementsByTagName('div');
for (var i = 0, div; div = divs[i]; i++) {
  /* Process div in some way */
}
```

 This avoids the overhead of checking the length of the array, and ensures that the `div` variable is reassigned to the current item each time around the loop for added convenience.

**Note**: Introduced in JavaScript 1.6

The [`forEach()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/forEach&action=edit&redlink=1) method, introduced in JavaScript 1.6, provides another way of iterating over an array:

``` js
var colors = ['red', 'green', 'blue'];
colors.forEach(function(color) {
  console.log(color);
});
```

 The function passed to `forEach` is executed once for every item in the array, with the array item passed as the argument to the function. Unassigned values are not iterated in a `forEach` loop.

Since JavaScript elements are saved as standard object properties, it is not advisable to iterate through JavaScript arrays using for...in loops because normal elements and all enumerable properties will be listed.

### Array Methods

The `Array` object has the following methods:

[`concat()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/concat&action=edit&redlink=1) joins two arrays and returns a new array.

``` js
var myArray = new Array("1", "2", "3");
myArray = myArray.concat("a", "b", "c"); // myArray is now ["1", "2", "3", "a", "b", "c"]
```

[`join(deliminator = ",")`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/join&action=edit&redlink=1) joins all elements of an array into a string.

``` js
var myArray = new Array("Wind", "Rain", "Fire");
var list = myArray.join(" - "); // list is "Wind - Rain - Fire"
```

[`push()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/push&action=edit&redlink=1) adds one or more elements to the end of an array and returns the resulting length of the array.

``` js
var myArray = new Array("1", "2");
 myArray.push("3"); // MyArray is now ["1", "2", "3"]
```

[`pop()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/pop&action=edit&redlink=1) removes the last element from an array and returns that element.

``` js
var myArray = new Array("1", "2", "3");
var last = myArray.pop(); // MyArray is now ["1", "2"], last = "3"
```

[`shift()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/shift&action=edit&redlink=1) removes the first element from an array and returns that element

``` js
var myArray = new Array ("1", "2", "3");
var first = myArray.shift(); // MyArray is now ["2", "3"], first is "1"
```

[`unshift()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/unshift&action=edit&redlink=1) adds one or more elements to the front of an array and returns the new length of the array.

``` js
var myArray = new Array ("1", "2", "3");
myArray.unshift("4", "5"); // myArray becomes ["4", "5", "1", "2", "3"]
```

[`slice(start_index, upto_index)`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/slice&action=edit&redlink=1) extracts a section of an array and returns a new array.

``` js
var myArray = new Array ("a", "b", "c", "d", "e");
myArray = myArray.slice(1, 4); /* starts at index 1 and extracts all elements
  until index 3, returning [ "b", "c", "d"] */
```

[`splice(index, count_to_remove, addelement1, addelement2, ...)`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/splice&action=edit&redlink=1) removes elements from an array and (optionally) replaces them.

``` js
var myArray = new Array ("1", "2", "3", "4", "5");
myArray.splice(1, 3, "a", "b", "c", "d"); // MyArray is now ["1", "a", "b", "c", "d", "5"]
  // This code started at index one (or where the "2" was), removed 3 elements there,
  // and then inserted all consecutive elements in its place.
```

[`reverse()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/reverse&action=edit&redlink=1) transposes the elements of an array: the first array element becomes the last and the last becomes the first.

``` js
var myArray = new Array ("1", "2", "3");
myArray.reverse(); // transposes the array so that myArray = [ "3", "2", "1" ]
```

[`sort()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/sort&action=edit&redlink=1) sorts the elements of an array.

``` js
var myArray = new Array("Wind", "Rain", "Fire");
myArray.sort(); // sorts the array so that myArrray = [ "Fire", "Rain", "Wind" ]
```

`sort()`, however by default assumes the elements are strings. If given an array of numbers, sort may return incorrect results.

``` js
var myArray = new Array(4, 8, 12, 16, 20, 24);
myArray.sort(); // returns myArrray = [ 12, 16, 20, 24, 4, 8]
```

 The above is obviously incorrect. Fortunately `sort()` can also take a callback function to determine how array elements are compared. The function compares two values and returns one of three values:

-   if `a` is less than `b` by the sorting system, return -1 (or any negative number)
-   if `a` is greater than `b` by the sorting system, return 1 (or any positive number)
-   if `a` and `b` are considered equivalent, return 0. For, instance, the following will sort by the last letter of an array:

The above problem number sorting problem can then be easily handled like so.

``` js
var myArray = new Array(4, 8, 12, 16, 20, 24);
var sortFn = function(a, b){
   return a-b;
 }
myArray.sort(sortFn); // returns myArrray = [4, 8, 12, 16, 20, 24] like it should
```

The sorting function thus provides a way to sort arrays any way the user likes. For example say we want to sort the first string array in reverse alphabetical order.

``` js
var sortFn = function(a, b){
   if (a[a.length - 1] < b[b.length - 1]) return -1;
   if (a[a.length - 1] > b[b.length - 1]) return 1;
   if (a[a.length - 1] == b[b.length - 1]) return 0;
 }
 myArray.sort(sortFn); // sorts the array so that myArray = ["Wind","Fire","Rain"]
```

**Note**: Introduced in JavaScript 1.6

 Compatibility code for older browsers can be found for each of these functions on the individual pages. Native browser support for these features in various browsers can be found [here.](http://www.robertnyman.com/javascript/)

[`indexOf(searchElement[, fromIndex])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/indexOf&action=edit&redlink=1) searches the array for `searchElement` and returns the index of the first match.

``` js
var a = ['a', 'b', 'a', 'b', 'a'];
alert(a.indexOf('b')); // Alerts 1
// Now try again, starting from after the last match
alert(a.indexOf('b', 2)); // Alerts 3
alert(a.indexOf('z')); // Alerts -1, because 'z' was not found
```

[`lastIndexOf(searchElement[, fromIndex])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/lastIndexOf&action=edit&redlink=1) works like `indexOf`, but starts at the end and searches backwards.

``` js
var a = ['a', 'b', 'c', 'd', 'a', 'b'];
alert(a.lastIndexOf('b')); // Alerts 5
// Now try again, starting from before the last match
alert(a.lastIndexOf('b', 4)); // Alerts 1
alert(a.lastIndexOf('z')); // Alerts -1
```

[`forEach(callback[, thisObject])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/forEach&action=edit&redlink=1) execute `callback` on every array item.

``` js
var a = ['a', 'b', 'c'];
a.forEach(alert); // Alerts each item in turn
```

[`map(callback[, thisObject])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/map&action=edit&redlink=1) returns a new array of the return value from executing `callback` on every array item.

``` js
var a1 = ['a', 'b', 'c'];
var a2 = a1.map(function(item) { return item.toUpperCase(); });
alert(a2); // Alerts A,B,C
```

[`filter(callback[, thisObject])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/filter&action=edit&redlink=1) returns a new array containing the items for which callback returned true.

``` js
var a1 = ['a', 10, 'b', 20, 'c', 30];
var a2 = a1.filter(function(item) { return typeof item == 'number'; });
alert(a2); // Alerts 10,20,30
```

[`every(callback[, thisObject])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/every&action=edit&redlink=1) returns true if `callback` returns true for every item in the array.

``` js
function isNumber(value){
  return typeof value == 'number';
}
var a1 = [1, 2, 3];
alert(a1.every(isNumber)); // Alerts true
var a2 = [1, '2', 3];
alert(a2.every(isNumber)); // Alerts false
```

[`some(callback[, thisObject])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/some&action=edit&redlink=1) returns true if `callback` returns true for at least one item in the array.

``` js
function isNumber(value){
  return typeof value == 'number';
}
var a1 = [1, 2, 3];
alert(a1.some(isNumber)); // Alerts true
var a2 = [1, '2', 3];
alert(a2.some(isNumber)); // Alerts true
var a3 = ['1', '2', '3'];
alert(a3.some(isNumber)); // Alerts false
```

 The methods above that take a callback are known as *iterative methods*, because they iterate over the entire array in some fashion. Each one takes an optional second argument called `thisObject`. If provided, `thisObject` becomes the value of the `this` keyword inside the body of the callback function. If not provided, as with other cases where a function is invoked outside of an explicit object context, `this` will refer to the global object ([`window`](/en-US/docs/DOM/window)).

The callback function is actually called with three arguments. The first is the value of the current item, the second is its array index and the third is a reference to the array itself. JavaScript functions ignore any arguments that are not named in the parameter list so it is safe to provide a callback function that only takes a single argument, such as `alert`.

**Note**: Introduced in JavaScript 1.8

[`reduce(callback[, initialValue])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/Reduce&action=edit&redlink=1) applies `callback(firstValue, secondValue)` to reduce the list of items down to a single value.

``` js
var a = [10, 20, 30];
var total = a.reduce(function(first, second) { return first + second; }, 0);
alert(total) // Alerts 60
```

[`reduceRight(callback[, initialValue])`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/ReduceRight&action=edit&redlink=1) works like `reduce()`, but starts with the last element.

`reduce` and `reduceRight` are the least obvious of the iterative array methods. They should be used for algorithms that combine two values recursively in order to reduce a sequence down to a single value.

### Multi-Dimensional Arrays

Arrays can be nested, meaning that an array can contian another array as an element. Using this characteristic of JavaScript arrays, multi-dimensional arrays can be created.

The following code creates a two-dimensional array:

``` js
var a = new Array(4);
for (i = 0; i < 4; i++) {
  a[i] = new Array(4);
  for (j = 0; j < 4; j++) {
    a[i][j] = "[" + i + "," + j + "]";
  }
}
```

 This example creates an array with the following rows:

    Row 0: [0,0] [0,1] [0,2] [0,3]
    Row 1: [1,0] [1,1] [1,2] [1,3]
    Row 2: [2,0] [2,1] [2,2] [2,3]
    Row 3: [3,0] [3,1] [3,2] [3,3]

### Arrays and Regular Expressions

When an array is the result of a match between a regular expression and a string, the array returns properties and elements that provide information about the match. An array is the return value of [`RegExp.exec()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/RegExp/exec&action=edit&redlink=1), [`String.match()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/String/match&action=edit&redlink=1), and [`String.split()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/String/split&action=edit&redlink=1). For information on using arrays with regular expressions, see [Regular Expressions](/concepts/programming/javascript/regex).

### Working with Array-like objects

**Note**: Introduced in JavaScript 1.6

 Some JavaScript objects, such as the [`NodeList`](/w/index.php?title=concepts/programming/javascript/core_objects/dom/NodeList&action=edit&redlink=1) returned by [`document.getElementsByTagName()`](/w/index.php?title=concepts/programming/javascript/core_objects/dom/document.getElementsByTagName&action=edit&redlink=1) or the [`arguments`](/w/index.php?title=concepts/programming/javascript/core_objects/sj/functions/arguments&action=edit&redlink=1) object made available within the body of a function, look and behave like arrays on the surface but do not share all of their methods. The `arguments` object provides a [`length`](/w/index.php?title=concepts/programming/javascript/core_objects/js/functions/arguments/length&action=edit&redlink=1) attribute but does not implement the [`forEach()`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/Array/forEach&action=edit&redlink=1) method, for example.

Array generics, introduced in JavaScript 1.6, provide a way of running `Array` methods against other array-like objects. Each standard array method has a corresponding method on the `Array` object itself; for example:

``` js
function alertArguments() {
  Array.forEach(arguments, function(item) {
    alert(item);
  });
}
```

 These generic methods can be emulated more verbosely in older versions of JavaScript using the call method provided by JavaScript function objects:

``` js
Array.prototype.forEach.call(arguments, function(item) {
  alert(item);
});
```

 Array generic methods can be used on strings as well, since they provide sequential access to their characters in a similar way to arrays:

``` js
Array.forEach("a string", function(chr) {
  alert(chr);
});
```

 Here are some further examples of applying array methods to strings, also taking advantage of expression closures:

``` js
var str = 'abcdef';
var consonantsOnlyStr = Array.filter(str, function (c) !(/[aeiou]/i).test(c)).join(''); // 'bcdf'
var vowelsPresent = Array.some(str, function (c) (/[aeiou]/i).test(c)); // true
var allVowels = Array.every(str, function (c) (/[aeiou]/i).test(c)); // false
var interpolatedZeros = Array.map(str, function (c) c+'0').join(''); // 'a0b0c0d0e0f0'
var numerologicalValue = Array.reduce(str, function (c, c2) c+c2.toLowerCase().charCodeAt()-96, 0);
// 21 (reduce() since JS v1.8)
```

 Note that `filter` and `map` do not automatically return the characters back into being members of a string in the return result; an array is returned, so we must use `join` to return back to a string.

### Array comprehensions

**Note**: Introduced in JavaScript 1.7

Introduced in JavaScript 1.7, array comprehensions provide a useful shortcut for constructing a new array based on the contents of another. Comprehensions can often be used in place of calls to `map()` and `filter()`, or as a way of combining the two.

The following comprehension takes an array of numbers and creates a new array of the double of each of those numbers.

``` js
var numbers = [1, 2, 3, 4];
var doubled = [i * 2 for each (i in numbers)];
alert(doubled); // Alerts 2,4,6,8
```

 This is equivalent to the following `map()` operation:

``` js
var doubled = numbers.map(function(i) { return i * 2; });
```

 Comprehensions can also be used to select items that match a particular expression. Here is a comprehension which selects only even numbers:

``` js
var numbers = [1, 2, 3, 21, 22, 30];
var evens = [i for each (i in numbers) if (i % 2 == 0)];
alert(evens); // Alerts 2,22,30
```

`filter()` can be used for the same purpose:

``` js
var evens = numbers.filter(function(i) { return i % 2 == 0; });
```

`map()` and `filter()` style operations can be combined into a single array comprehension. Here is one that filters just the even numbers, then creates an array containing their doubles:

``` js
var numbers = [1, 2, 3, 21, 22, 30];
var doubledEvens = [i * 2 for each (i in numbers) if (i % 2 == 0)];
alert(doubledEvens); // Alerts 4,44,60
```

 The square brackets of an array comprehension introduce an implicit block for scoping purposes. New variables (such as i in the example) are treated as if they had been declared using `let`. This means that they will not be available outside of the comprehension.

The input to an array comprehension does not itself need to be an array; [iterators and generators](/w/index.php?title=concepts/programming/javascript/core_objects/guides/JavaScript/Iterators&action=edit&redlink=1) can also be used.

Even strings may be used as input; to achieve the filter and map actions (under Array-like objects) above:

``` js
var str = 'abcdef';
var consonantsOnlyStr = [c for each (c in str) if (!(/[aeiouAEIOU]/).test(c))  ].join(''); // 'bcdf'
var interpolatedZeros = [c+'0' for each (c in str) ].join(''); // 'a0b0c0d0e0f0'
```

 Again, the input form is not preserved, so we have to use `join()` to revert back to a string.

## Boolean Object

The `Boolean` object is a wrapper around the primitive Boolean data type. Use the following syntax to create a `Boolean` object:

``` js
var booleanObjectName = new Boolean(value);
```

 Do not confuse the primitive Boolean values `true` and `false` with the true and false values of the `Boolean` object. Any object whose value is not `undefined`, `null`, `0`, `NaN`, or the empty string , including a `Boolean` object whose value is false, evaluates to true when passed to a conditional statement. See [if...else Statement](/w/index.php?title=guides/JavaScript/Statements&action=edit&redlink=1) for more information.

## Date Object

JavaScript does not have a date data type. However, you can use the `Date` object and its methods to work with dates and times in your applications. The `Date` object has a large number of methods for setting, getting, and manipulating dates. It does not have any properties.

JavaScript handles dates similarly to Java. The two languages have many of the same date methods, and both languages store dates as the number of milliseconds since January 1, 1970, 00:00:00.

The `Date` object range is -100,000,000 days to 100,000,000 days relative to 01 January, 1970 UTC.

To create a `Date` object:

``` js
var dateObjectName = new Date([parameters]);
```

 where `dateObjectName` is the name of the `Date` object being created; it can be a new object or a property of an existing object.

Calling Date without the new keyword simply converts the provided date to a string representation.

The `parameters` in the preceding syntax can be any of the following:

-   Nothing: creates today's date and time. For example, `today = new Date();`.
-   A string representing a date in the following form: "Month day, year hours:minutes:seconds." For example, `var Xmas95 = new Date("December 25, 1995 13:30:00")`. If you omit hours, minutes, or seconds, the value will be set to zero.
-   A set of integer values for year, month, and day. For example, `var Xmas95 = new Date(1995, 11, 25)`.
-   A set of integer values for year, month, day, hour, minute, and seconds. For example, `var Xmas95 = new Date(1995, 11, 25, 9, 30, 0);`.

**JavaScript 1.2 and earlier**
 The `Date` object behaves as follows:

-   Dates prior to 1970 are not allowed.
-   JavaScript depends on platform-specific date facilities and behavior; the behavior of the `Date` object varies from platform to platform.

### Methods of the Date Object

The `Date` object methods for handling dates and times fall into these broad categories:

-   "set" methods, for setting date and time values in `Date` objects.
-   "get" methods, for getting date and time values from `Date` objects.
-   "to" methods, for returning string values from `Date` objects.
-   parse and UTC methods, for parsing `Date` strings.

With the "get" and "set" methods you can get and set seconds, minutes, hours, day of the month, day of the week, months, and years separately. There is a `getDay` method that returns the day of the week, but no corresponding `setDay` method, because the day of the week is set automatically. These methods use integers to represent these values as follows:

-   Seconds and minutes: 0 to 59
-   Hours: 0 to 23
-   Day: 0 (Sunday) to 6 (Saturday)
-   Date: 1 to 31 (day of the month)
-   Months: 0 (January) to 11 (December)
-   Year: years since 1900

For example, suppose you define the following date:

``` js
var Xmas95 = new Date("December 25, 1995");
```

 Then `Xmas95.getMonth()` returns 11, and `Xmas95.getFullYear()` returns 1995.

The `getTime` and `setTime` methods are useful for comparing dates. The `getTime` method returns the number of milliseconds since January 1, 1970, 00:00:00 for a `Date` object.

For example, the following code displays the number of days left in the current year:

``` js
var today = new Date();
var endYear = new Date(1995, 11, 31, 23, 59, 59, 999); // Set day and month
endYear.setFullYear(today.getFullYear()); // Set year to this year
var msPerDay = 24 * 60 * 60 * 1000; // Number of milliseconds per day
var daysLeft = (endYear.getTime() - today.getTime()) / msPerDay;
var daysLeft = Math.round(daysLeft); //returns days left in the year
```

 This example creates a `Date` object named `today` that contains today's date. It then creates a `Date` object named `endYear` and sets the year to the current year. Then, using the number of milliseconds per day, it computes the number of days between `today` and `endYear`, using `getTime` and rounding to a whole number of days.

The `parse` method is useful for assigning values from date strings to existing `Date` objects. For example, the following code uses `parse` and `setTime` to assign a date value to the `IPOdate` object:

``` js
var IPOdate = new Date();
IPOdate.setTime(Date.parse("Aug 9, 1995"));
```

### Using the Date Object: an Example

In the following example, the function `JSClock()` returns the time in the format of a digital clock.

``` js
function JSClock() {
  var time = new Date();
  var hour = time.getHours();
  var minute = time.getMinutes();
  var second = time.getSeconds();
  var temp = "" + ((hour > 12) ? hour - 12 : hour);
  if (hour == 0)
    temp = "12";
  temp += ((minute < 10) ? ":0" : ":") + minute;
  temp += ((second < 10) ? ":0" : ":") + second;
  temp += (hour >= 12) ? " P.M." : " A.M.";
  return temp;
 }
```

 The `JSClock` function first creates a new `Date` object called `time`; since no arguments are given, time is created with the current date and time. Then calls to the `getHours`, `getMinutes`, and `getSeconds` methods assign the value of the current hour, minute and seconds to `hour`, `minute`, and `second`.

The next four statements build a string value based on the time. The first statement creates a variable `temp`, assigning it a value using a conditional expression; if `hour` is greater than 12, (`hour - 12`), otherwise simply hour, unless hour is 0, in which case it becomes 12.

The next statement appends a `minute` value to `temp`. If the value of `minute` is less than 10, the conditional expression adds a string with a preceding zero; otherwise it adds a string with a demarcating colon. Then a statement appends a seconds value to `temp` in the same way.

Finally, a conditional expression appends "PM" to `temp` if `hour` is 12 or greater; otherwise, it appends "AM" to `temp`.

## Function Object

The predefined `Function` object specifies a string of JavaScript code to be compiled as a function.

To create a `Function` object:

``` js
var functionObjectName = new Function ([arg1, arg2, ... argn], functionBody);
```

`functionObjectName` is the name of a variable or a property of an existing object. It can also be an object followed by a lowercase event handler name, such as `window.onerror`.

`arg1`, `arg2`, ... `argn` are arguments to be used by the function as formal argument names. Each must be a string that corresponds to a valid JavaScript identifier; for example "x" or "theForm".

`functionBody` is a string specifying the JavaScript code to be compiled as the function body.

`Function` objects are evaluated each time they are used. This is less efficient than declaring a function and calling it within your code, because declared functions are compiled.

In addition to defining functions as described here, you can also use the [`function` statement](/w/index.php?title=concepts/programming/javascript/core_objects/js/statements/function&action=edit&redlink=1) and the function expression. See the [JavaScript Reference](/w/index.php?title=concepts/programming/javascript/core_objects/js&action=edit&redlink=1) for more information.

The following code assigns a function to the variable `setBGColor`. This function sets the current document's background color.

``` js
var setBGColor = new Function("document.bgColor = 'antiquewhite'");
```

 To call the `Function` object, you can specify the variable name as if it were a function. The following code executes the function specified by the `setBGColor` variable:

``` js
var colorChoice="antiquewhite";
if (colorChoice=="antiquewhite") {setBGColor()}
```

 You can assign the function to an event handler in either of the following ways:

``` js
document.form1.colorButton.onclick = setBGColor;
```

``` html
<INPUT NAME="colorButton" TYPE="button"
   VALUE="Change background color"
   onClick="setBGColor()">
```

 Creating the variable `setBGColor` shown above is similar to declaring the following function:

``` js
function setBGColor() {
  document.bgColor = 'antiquewhite';
}
```

 Assigning a function to a variable is similar to declaring a function, but there are differences:

-   When you assign a function to a variable using `var setBGColor = new Function("...")`, `setBGColor` is a variable for which the current value is a reference to the function created with `new Function()`.
-   When you create a function using `function setBGColor() {...}`, `setBGColor` is not a variable, it is the name of a function.

You can nest a function within a function. The nested (inner) function is private to its containing (outer) function:

-   The inner function can be accessed only from statements in the outer function.
-   The inner function can use the arguments and variables of the outer function. The outer function cannot use the arguments and variables of the inner function.

## Math Object

The predefined `Math` object has properties and methods for mathematical constants and functions. For example, the `Math` object's `PI` property has the value of pi (3.141...), which you would use in an application as

    Math.PI

Similarly, standard mathematical functions are methods of `Math`. These include trigonometric, logarithmic, exponential, and other functions. For example, if you want to use the trigonometric function sine, you would write

    Math.sin(1.56)

Note that all trigonometric methods of `Math` take arguments in radians.

The following table summarizes the `Math` object's methods.

|Method|Description|
|:-----|:----------|
|`abs`|Absolute value|
|`sin`, `cos`, `tan`|Standard trigonometric functions; argument in radians|
|`acos`, `asin`, `atan`, `atan2`|Inverse trigonometric functions; return values in radians|
|`exp`, `log`|Exponential and natural logarithm, base `e`|
|`ceil`|Returns least integer greater than or equal to argument|
|`floor`|Returns greatest integer less than or equal to argument|
|`min`, `max`|Returns greater or lesser (respectively) of two arguments|
|`pow`|Exponential; first argument is base, second is exponent|
|`random`|Returns a random number between 0 and 1.|
|`round`|Rounds argument to nearest integer|
|`sqrt`|Square root|

Unlike many other objects, you never create a `Math` object of your own. You always use the predefined `Math` object.

## Number Object

The `Number` object has properties for numerical constants, such as maximum value, not-a-number, and infinity. You cannot change the values of these properties and you use them as follows:

``` js
var biggestNum = Number.MAX_VALUE;
var smallestNum = Number.MIN_VALUE;
var infiniteNum = Number.POSITIVE_INFINITY;
var negInfiniteNum = Number.NEGATIVE_INFINITY;
var notANum = Number.NaN;
```

 You always refer to a property of the predefined `Number` object as shown above, and not as a property of a `Number` object you create yourself.

The following table summarizes the `Number` object's properties.

|Property|Description|
|:-------|:----------|
|`MAX_VALUE`|The largest representable number|
|`MIN_VALUE`|The smallest representable number|
|`NaN`|Special "not a number" value|
|`NEGATIVE_INFINITY`|Special negative infinite value; returned on overflow|
|`POSITIVE_INFINITY`|Special positive infinite value; returned on overflow|

The Number prototype provides methods for retrieving information from Number objects in various formats. The following table summarizes the methods of `Number.prototype`.

|Method|Description|
|:-----|:----------|
|`toExponential`|Returns a string representing the number in exponential notation.|
|`toFixed`|Returns a string representing the number in fixed-point notation.|
|`toPrecision`|Returns a string representing the number to a specified precision in fixed-point notation.|
|`toSource`|Returns an object literal representing the specified `Number` object; you can use this value to create a new object. Overrides the `Object.toSource` method.|
|`toString`|Returns a string representing the specified object. Overrides the `Object.toString `method.|
|`valueOf`|Returns the primitive value of the specified object. Overrides the `Object.valueOf `method.|

## RegExp Object

The `RegExp` object lets you work with regular expressions. It is described in [RegExp](/concepts/programming/javascript/regex).

## String Object

The `String` object is a wrapper around the string primitive data type. Do not confuse a string literal with the `String` object. For example, the following code creates the string literal `s1` and also the `String` object `s2`:

``` js
var s1 = "foo"; //creates a string literal value
var s2 = new String("foo"); //creates a String object
```

 You can call any of the methods of the `String` object on a string literal value—JavaScript automatically converts the string literal to a temporary `String` object, calls the method, then discards the temporary `String` object. You can also use the `String.length` property with a string literal.

You should use string literals unless you specifically need to use a `String` object, because `String` objects can have counterintuitive behavior. For example:

``` js
var s1 = "2 + 2"; //creates a string literal value
var s2 = new String("2 + 2"); //creates a String object
eval(s1); //returns the number 4
eval(s2); //returns the string "2 + 2"
```

 A `String` object has one property, `length`, that indicates the number of characters in the string. For example, the following code assigns `x` the value 13, because "Hello, World!" has 13 characters:

``` js
var mystring = "Hello, World!";
var x = mystring.length;
```

 A `String` object has two types of methods: those that return a variation on the string itself, such as `substring` and `toUpperCase`, and those that return an HTML-formatted version of the string, such as `bold` and `link`.

For example, using the previous example, both `mystring.toUpperCase()` and `"hello, world!".toUpperCase()` return the string "HELLO, WORLD!"

The `substring` method takes two arguments and returns a subset of the string between the two arguments. Using the previous example, `mystring.substring(4, 9)` returns the string "o, Wo". See the [`substring`](/w/index.php?title=concepts/programming/javascript/core_objects/js/objects/String/substring&action=edit&redlink=1) method of the `String` object in the JavaScript Reference for more information.

The `String` object also has a number of methods for automatic HTML formatting, such as `bold` to create boldface text and `link` to create a hyperlink. For example, you could create a hyperlink to a hypothetical URL with the `link` method as follows:

``` js
mystring.link("http://www.helloworld.com");
```

 The following table summarizes the methods of `String` objects.

|Method|Description|
|:-----|:----------|
|`anchor`|Creates HTML named anchor.|
|`big`, `blink`, `bold`, `fixed`, `italics`, `small`, `strike`, `sub`, `sup`|Create HTML formatted string.|
|`charAt`, `charCodeAt`|Return the character or character code at the specified position in string.|
|`indexOf`, `lastIndexOf`|Return the position of specified substring in the string or last position of specified substring, respectively.|
|`link`|Creates HTML hyperlink.|
|`concat`|Combines the text of two strings and returns a new string.|
|`fromCharCode`|Constructs a string from the specified sequence of Unicode values. This is a method of the String class, not a String instance.|
|`split`|Splits a `String` object into an array of strings by separating the string into substrings.|
|`slice`|Extracts a section of an string and returns a new string.|
|`substring`, `substr`|Return the specified subset of the string, either by specifying the start and end indexes or the start index and a length.|
|`match`, `replace`, `search`|Work with regular expressions.|
|`toLowerCase`, `toUpperCase`|Return the string in all lowercase or all uppercase, respectively.|

<span style="float: left">[« Previous](/w/index.php?title=concepts/programming/javascript/core_objects/guides/JavaScript/Working_with_Objects&action=edit&redlink=1)</span>[Next »](/w/index.php?title=concepts/programming/javascript/core_objects/guides/JavaScript/Details_of_the_Object_Model&action=edit&redlink=1)

