{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|This chapter describes the predefined objects in core JavaScript: <code>Array</code>, <code>Boolean</code>, <code>Date</code>, <code>Function</code>, <code>Math</code>, <code>Number</code>, <code>RegExp</code>, and <code>String</code>.}}
{{Tutorial
|Content===Array Object==

JavaScript does not have an explicit array data type. However, you can use the predefined <code>Array</code> object and its methods to work with arrays in your applications. The <code>Array</code> object has methods for manipulating arrays in various ways, such as joining, reversing, and sorting them. It has a property for determining the array length and other properties for use with regular expressions.

An ''array'' is an ordered set of values that you refer to with a name and an index. For example, you could have an array called <code>emp</code> that contains employees' names indexed by their employee number. So <code>emp[1]</code> would be employee number one, <code>emp[2]</code> employee number two, and so on.

===Creating an Array===

To create an <code>Array</code> object, the following three statements are equivalent:

<syntaxhighlight lang="javascript">
var arr = new Array(element0, element1, ..., elementN);
var arr = Array(element0, element1, ..., elementN);
var arr = [element0, element1, ..., elementN];
</syntaxhighlight>

<code>element0, element1, ..., elementN</code> is a list of values for the array's elements. When this form is specified, the array is initialized with the specified values as its elements, and the array's <code>length</code> property is set to the number of arguments.

The bracket syntax is called "array literal" or "array initializer". It is shorter and so is generally preferred. See [[/guides/js/Values#Array_Literals|Array Literals]] for details on array literals.

To create an Array with non-zero length, but without any items, either of the following can be used:

<syntaxhighlight lang="javascript">
var arr = new Array(arrayLength);
var arr = Array(arrayLength);
 
 // This has exactly the same effect
var arr = [];
arr.length = arrayLength;
</syntaxhighlight>

Note: in the above code, <code>arrayLength</code> must be a <code>Number</code>. Otherwise, an array with a single element (the provided value) will be created. Calling <code>arr.length</code> will return <code>arrayLength</code>, but the array actually contains empty (undefined) elements. Running a for...in loop on the array will return none of the array's elements.

In addition to a newly defined variable as shown above, Arrays can also be assigned as a property of a new or an existing object:

<syntaxhighlight lang="javascript">
var obj = {};
// ...
obj.prop = [element0, element1, ..., elementN];
 
// OR
var obj = {prop: [element0, element1, ...., elementN]}
</syntaxhighlight>

If you wish to initialize an array with a single element, and the element happens to be a <code>Number</code>, you must use the bracket syntax. When a single <code>Number</code> value is passed to the Array() constructor or function, it is interpreted as an <code>arrayLength</code>, not as a single element.

<syntaxhighlight lang="javascript">
var arr = [42];
var arr = Array(42); // Creates an array with no element, but with arr.length set to 42 

// The above code is equivalent to
var arr = [];
arr.length = 42;
</syntaxhighlight>

Furthermore, if you are creating an array with a single element, and the element happens to be a non-whole <code>Number</code> (a number with a non-trivial floating part), a <code>RangeError</code> is thrown. If there is a possibility that your code will be creating arrays with single elements, with arbitrary data type, it is safer to use array literals, or create an empty array first and then fill it up.

<syntaxhighlight lang="javascript">
var arr = Array(9.3);  // RangeError: Invalid array length
</syntaxhighlight>

===Populating an Array===

You can populate an array by assigning values to its elements. For example:

<syntaxhighlight lang="javascript">
var emp = [];
emp[0] = "Casey Jones";
emp[1] = "Phil Lesh";
emp[2] = "August West";
</syntaxhighlight>

'''Note:''' if you supply a non-integer value to the array operator in the code above, a property will be created in the object representing the array, instead of an array element.

<syntaxhighlight lang="javascript">
var arr = [];
arr[3.4] = "Oranges";
console.log(arr.length);                // 0
console.log(arr.hasOwnProperty[3.4]);   // true
</syntaxhighlight>

You can also populate an array when you create it:

<syntaxhighlight lang="javascript">
var myArray = new Array("Hello", myVar, 3.14159);
var myArray = ["Mango", "Apple", "Orange"];
</syntaxhighlight>

===Referring to Array Elements===

You refer to an array's elements by using the element's ordinal number. For example, suppose you define the following array:

<syntaxhighlight lang="javascript">
var myArray = ["Wind", "Rain", "Fire"];
</syntaxhighlight>

You then refer to the first element of the array as <code>myArray[0]</code> and the second element of the array as <code>myArray[1]</code>. The index of the elements begins with zero.

{{Note| The array operator (square brackets) is also used for accessing the array's properties (arrays are also objects in JavaScript). For example,}}

<syntaxhighlight lang="javascript">
var arr = ["one", "two", "three"];
arr[2];  // three
arr["length"];  // 3
</syntaxhighlight>

===Understanding length===

At the implementation level, JavaScript's arrays actually store their elements as standard object properties, using the array index as the property name. The <code>length</code> property is special; it always returns the index of the last element. Remember, Javascript Array indexes are 0-based: they start at 0, not 1. This means that the <code>length</code> property will be one more than the highest index stored in the array:

<syntaxhighlight lang="javascript">
var cats = [];
cats[30] = ['Dusty'];
print(cats.length); // 31
</syntaxhighlight>

You can also assign to the <code>length</code> property. Writing a value that is shorter than the number of stored items truncates the array; writing 0 empties it entirely:

<syntaxhighlight lang="javascript">
var cats = ['Dusty', 'Misty', 'Twiggy'];
console.log(cats.length); // 3
 
cats.length = 2;
console.log(cats); // prints "Dusty,Misty" - Twiggy has been removed
 
cats.length = 0;
console.log(cats); // prints nothing; the cats array is empty
 
cats.length = 3;
console.log(cats);  // [undefined, undefined, undefined]
</syntaxhighlight>

===Iterating over arrays===

A common operation is to iterate over the values of an array, processing each one in some way. The simplest way to do this is as follows:

<syntaxhighlight lang="javascript">
var colors = ['red', 'green', 'blue'];
for (var i = 0; i < colors.length; i++) {
  console.log(colors[i]);
}
</syntaxhighlight>

If you know that none of the elements in your array evaluate to <code>false</code> in a boolean context — if your array consists only of [[/dom|DOM]] nodes for example, you can use a more efficient idiom:

<syntaxhighlight lang="javascript">
var divs = document.getElementsByTagName('div');
for (var i = 0, div; div = divs[i]; i++) {
  /* Process div in some way */
}
</syntaxhighlight>

This avoids the overhead of checking the length of the array, and ensures that the <code>div</code> variable is reassigned to the current item each time around the loop for added convenience.

{{Note|Introduced in JavaScript 1.6}}


The [[/js/objects/Array/forEach|<code>forEach()</code>]] method, introduced in JavaScript 1.6, provides another way of iterating over an array:

<syntaxhighlight lang="javascript">
var colors = ['red', 'green', 'blue'];
colors.forEach(function(color) {
  console.log(color);
});
</syntaxhighlight>

The function passed to <code>forEach</code> is executed once for every item in the array, with the array item passed as the argument to the function. Unassigned values are not iterated in a <code>forEach</code> loop.

Since JavaScript elements are saved as standard object properties, it is not advisable to iterate through JavaScript arrays using for...in loops because normal elements and all enumerable properties will be listed.

===Array Methods===

The <code>Array</code> object has the following methods:

[[/js/objects/Array/concat|<code>concat()</code>]] joins two arrays and returns a new array.
<syntaxhighlight lang="javascript">
var myArray = new Array("1", "2", "3");
myArray = myArray.concat("a", "b", "c"); // myArray is now ["1", "2", "3", "a", "b", "c"]
</syntaxhighlight>

[[/js/objects/Array/join|<code>join(deliminator = ",")</code>]] joins all elements of an array into a string.
<syntaxhighlight lang="javascript">
var myArray = new Array("Wind", "Rain", "Fire");
var list = myArray.join(" - "); // list is "Wind - Rain - Fire"
</syntaxhighlight>

[[/js/objects/Array/push|<code>push()</code>]] adds one or more elements to the end of an array and returns the resulting length of the array.
<syntaxhighlight lang="javascript">
var myArray = new Array("1", "2");
 myArray.push("3"); // MyArray is now ["1", "2", "3"]
</syntaxhighlight>

[[/js/objects/Array/pop|<code>pop()</code>]] removes the last element from an array and returns that element.
<syntaxhighlight lang="javascript">
var myArray = new Array("1", "2", "3");
var last = myArray.pop(); // MyArray is now ["1", "2"], last = "3"
</syntaxhighlight>

[[/js/objects/Array/shift|<code>shift()</code>]] removes the first element from an array and returns that element
<syntaxhighlight lang="javascript">
var myArray = new Array ("1", "2", "3");
var first = myArray.shift(); // MyArray is now ["2", "3"], first is "1"
</syntaxhighlight>

[[/js/objects/Array/unshift|<code>unshift()</code>]] adds one or more elements to the front of an array and returns the new length of the array.
<syntaxhighlight lang="javascript">
var myArray = new Array ("1", "2", "3");
myArray.unshift("4", "5"); // myArray becomes ["4", "5", "1", "2", "3"]
</syntaxhighlight>

[[/js/objects/Array/slice|<code>slice(start_index, upto_index)</code>]] extracts a section of an array and returns a new array.
<syntaxhighlight lang="javascript">
var myArray = new Array ("a", "b", "c", "d", "e");
myArray = myArray.slice(1, 4); /* starts at index 1 and extracts all elements
  until index 3, returning [ "b", "c", "d"] */
</syntaxhighlight>

[[/js/objects/Array/splice|<code>splice(index, count_to_remove, addelement1, addelement2, ...)</code>]] removes elements from an array and (optionally) replaces them.
<syntaxhighlight lang="javascript">
var myArray = new Array ("1", "2", "3", "4", "5");
myArray.splice(1, 3, "a", "b", "c", "d"); // MyArray is now ["1", "a", "b", "c", "d", "5"]
  // This code started at index one (or where the "2" was), removed 3 elements there, 
  // and then inserted all consecutive elements in its place.
</syntaxhighlight>

[[/js/objects/Array/reverse|<code>reverse()</code>]] transposes the elements of an array: the first array element becomes the last and the last becomes the first.
<syntaxhighlight lang="javascript">
var myArray = new Array ("1", "2", "3");
myArray.reverse(); // transposes the array so that myArray = [ "3", "2", "1" ]
</syntaxhighlight>

[[/js/objects/Array/sort|<code>sort()</code>]] sorts the elements of an array.
<syntaxhighlight lang="javascript">
var myArray = new Array("Wind", "Rain", "Fire");
myArray.sort(); // sorts the array so that myArrray = [ "Fire", "Rain", "Wind" ]
</syntaxhighlight>

<code>sort()</code> can also take a callback function to determine how array elements are compared. The function compares two values and returns one of three values:
* if <code>a</code> is less than <code>b</code> by the sorting system, return -1 (or any negative number)
* if <code>a</code> is greater than <code>b</code> by the sorting system, return 1 (or any positive number)
* if <code>a</code> and <code>b</code> are considered equivalent, return 0. For, instance, the following will sort by the last letter of an array:
<syntaxhighlight lang="javascript">
var sortFn = function(a, b){
   if (a[a.length - 1] < b[b.length - 1]) return -1;
   if (a[a.length - 1] > b[b.length - 1]) return 1;
   if (a[a.length - 1] == b[b.length - 1]) return 0;
 }
 myArray.sort(sortFn); // sorts the array so that myArray = ["Wind","Fire","Rain"]
</syntaxhighlight>

{{Note|Introduced in JavaScript 1.6}}

Compatibility code for older browsers can be found for each of these functions on the individual pages. Native browser support for these features in various browsers can be found [http://www.robertnyman.com/javascript/  here.]

[[/js/objects/Array/indexOf|<code>indexOf(searchElement[, fromIndex])</code>]] searches the array for <code>searchElement</code> and returns the index of the first match.
<syntaxhighlight lang="javascript">
var a = ['a', 'b', 'a', 'b', 'a'];
alert(a.indexOf('b')); // Alerts 1
// Now try again, starting from after the last match
alert(a.indexOf('b', 2)); // Alerts 3
alert(a.indexOf('z')); // Alerts -1, because 'z' was not found
</syntaxhighlight>

[[/js/objects/Array/lastIndexOf|<code>lastIndexOf(searchElement[, fromIndex])</code>]] works like <code>indexOf</code>, but starts at the end and searches backwards.
<syntaxhighlight lang="javascript">
var a = ['a', 'b', 'c', 'd', 'a', 'b'];
alert(a.lastIndexOf('b')); // Alerts 5
// Now try again, starting from before the last match
alert(a.lastIndexOf('b', 4)); // Alerts 1
alert(a.lastIndexOf('z')); // Alerts -1
</syntaxhighlight>

[[/js/objects/Array/forEach|<code>forEach(callback[, thisObject])</code>]] execute <code>callback</code> on every array item.
<syntaxhighlight lang="javascript">
var a = ['a', 'b', 'c'];
a.forEach(alert); // Alerts each item in turn
</syntaxhighlight>

[[/js/objects/Array/map|<code>map(callback[, thisObject])</code>]] returns a new array of the return value from executing <code>callback</code> on every array item.
<syntaxhighlight lang="javascript">
var a1 = ['a', 'b', 'c'];
var a2 = a1.map(function(item) { return item.toUpperCase(); });
alert(a2); // Alerts A,B,C
</syntaxhighlight>

[[/js/objects/Array/filter|<code>filter(callback[, thisObject])</code>]] returns a new array containing the items for which callback returned true.
<syntaxhighlight lang="javascript">
var a1 = ['a', 10, 'b', 20, 'c', 30];
var a2 = a1.filter(function(item) { return typeof item == 'number'; });
alert(a2); // Alerts 10,20,30
</syntaxhighlight>

[[/js/objects/Array/every|<code>every(callback[, thisObject])</code>]] returns true if <code>callback</code> returns true for every item in the array.
<syntaxhighlight lang="javascript">
function isNumber(value){
  return typeof value == 'number';
}
var a1 = [1, 2, 3];
alert(a1.every(isNumber)); // Alerts true
var a2 = [1, '2', 3];
alert(a2.every(isNumber)); // Alerts false
</syntaxhighlight>

[[/js/objects/Array/some|<code>some(callback[, thisObject])</code>]] returns true if <code>callback</code> returns true for at least one item in the array.
<syntaxhighlight lang="javascript">
function isNumber(value){
  return typeof value == 'number';
}
var a1 = [1, 2, 3];
alert(a1.some(isNumber)); // Alerts true
var a2 = [1, '2', 3];
alert(a2.some(isNumber)); // Alerts true
var a3 = ['1', '2', '3'];
alert(a3.some(isNumber)); // Alerts false
</syntaxhighlight>

The methods above that take a callback are known as ''iterative methods'', because they iterate over the entire array in some fashion. Each one takes an optional second argument called <code>thisObject</code>. If provided, <code>thisObject</code> becomes the value of the <code>this</code> keyword inside the body of the callback function. If not provided, as with other cases where a function is invoked outside of an explicit object context, <code>this</code> will refer to the global object ([http://docs.webplatform.org/en-US/docs/DOM/window <code>window</code>]).

The callback function is actually called with three arguments. The first is the value of the current item, the second is its array index and the third is a reference to the array itself. JavaScript functions ignore any arguments that are not named in the parameter list so it is safe to provide a callback function that only takes a single argument, such as <code>alert</code>.

{{Note|Introduced in JavaScript 1.8}}


[[/js/objects/Array/Reduce|<code>reduce(callback[, initialValue])</code>]] applies <code>callback(firstValue, secondValue)</code> to reduce the list of items down to a single value.
<syntaxhighlight lang="javascript">
var a = [10, 20, 30];
var total = a.reduce(function(first, second) { return first + second; }, 0);
alert(total) // Alerts 60
</syntaxhighlight>

[[/js/objects/Array/ReduceRight|<code>reduceRight(callback[, initialValue])</code>]] works like <code>reduce()</code>, but starts with the last element.

<code>reduce</code> and <code>reduceRight</code> are the least obvious of the iterative array methods. They should be used for algorithms that combine two values recursively in order to reduce a sequence down to a single value.

===Multi-Dimensional Arrays===

Arrays can be nested, meaning that an array can contian another array as an element. Using this characteristic of JavaScript arrays, multi-dimensional arrays can be created.

The following code creates a two-dimensional array:
<syntaxhighlight lang="javascript">
var a = new Array(4);
for (i = 0; i < 4; i++) {
  a[i] = new Array(4);
  for (j = 0; j < 4; j++) {
    a[i][j] = "[" + i + "," + j + "]";
  }
}
</syntaxhighlight>

This example creates an array with the following rows:

 Row 0: [0,0] [0,1] [0,2] [0,3]
 Row 1: [1,0] [1,1] [1,2] [1,3]
 Row 2: [2,0] [2,1] [2,2] [2,3]
 Row 3: [3,0] [3,1] [3,2] [3,3]

===Arrays and Regular Expressions===

When an array is the result of a match between a regular expression and a string, the array returns properties and elements that provide information about the match. An array is the return value of [[/js/objects/RegExp/exec|<code>RegExp.exec()</code>]], [[/js/objects/String/match|<code>String.match()</code>]], and [[/js/objects/String/split|<code>String.split()</code>]]. For information on using arrays with regular expressions, see [[/guides/JavaScript/RegEx|Regular Expressions]].

===Working with Array-like objects===

{{Note|Introduced in JavaScript 1.6}}

Some JavaScript objects, such as the [[/dom/NodeList|<code>NodeList</code>]] returned by [[/dom/document.getElementsByTagName|<code>document.getElementsByTagName()</code>]] or the [[/sj/functions/arguments|<code>arguments</code>]] object made available within the body of a function, look and behave like arrays on the surface but do not share all of their methods. The <code>arguments</code> object provides a [[/js/functions/arguments/length|<code>length</code>]] attribute but does not implement the [[/js/objects/Array/forEach|<code>forEach()</code>]] method, for example.

Array generics, introduced in JavaScript 1.6, provide a way of running <code>Array</code> methods against other array-like objects. Each standard array method has a corresponding method on the <code>Array</code> object itself; for example:

<syntaxhighlight lang="javascript">
function alertArguments() {
  Array.forEach(arguments, function(item) {
    alert(item);
  });
}
</syntaxhighlight>

These generic methods can be emulated more verbosely in older versions of JavaScript using the call method provided by JavaScript function objects:

<syntaxhighlight lang="javascript">
Array.prototype.forEach.call(arguments, function(item) {
  alert(item);
});
</syntaxhighlight>

Array generic methods can be used on strings as well, since they provide sequential access to their characters in a similar way to arrays:

<syntaxhighlight lang="javascript">
Array.forEach("a string", function(chr) {
  alert(chr);
});
</syntaxhighlight>

Here are some further examples of applying array methods to strings, also taking advantage of expression closures<nowiki>:</nowiki>

<syntaxhighlight lang="javascript">
var str = 'abcdef';
var consonantsOnlyStr = Array.filter(str, function (c) !(/[aeiou]/i).test(c)).join(''); // 'bcdf'
var vowelsPresent = Array.some(str, function (c) (/[aeiou]/i).test(c)); // true
var allVowels = Array.every(str, function (c) (/[aeiou]/i).test(c)); // false
var interpolatedZeros = Array.map(str, function (c) c+'0').join(''); // 'a0b0c0d0e0f0'
var numerologicalValue = Array.reduce(str, function (c, c2) c+c2.toLowerCase().charCodeAt()-96, 0);
// 21 (reduce() since JS v1.8)
</syntaxhighlight>

Note that <code>filter</code> and <code>map</code> do not automatically return the characters back into being members of a string in the return result; an array is returned, so we must use <code>join</code> to return back to a string.

===Array comprehensions===

{{Note|Introduced in JavaScript 1.7}}


Introduced in JavaScript 1.7, array comprehensions provide a useful shortcut for constructing a new array based on the contents of another. Comprehensions can often be used in place of calls to <code>map()</code> and <code>filter()</code>, or as a way of combining the two.

The following comprehension takes an array of numbers and creates a new array of the double of each of those numbers.

<syntaxhighlight lang="javascript">
var numbers = [1, 2, 3, 4];
var doubled = [i * 2 for each (i in numbers)];
alert(doubled); // Alerts 2,4,6,8
</syntaxhighlight>

This is equivalent to the following <code>map()</code> operation:

<syntaxhighlight lang="javascript">
var doubled = numbers.map(function(i) { return i * 2; });
</syntaxhighlight>

Comprehensions can also be used to select items that match a particular expression. Here is a comprehension which selects only even numbers:

<syntaxhighlight lang="javascript">
var numbers = [1, 2, 3, 21, 22, 30];
var evens = [i for each (i in numbers) if (i % 2 == 0)];
alert(evens); // Alerts 2,22,30
</syntaxhighlight>

<code>filter()</code> can be used for the same purpose:

<syntaxhighlight lang="javascript">
var evens = numbers.filter(function(i) { return i % 2 == 0; });
</syntaxhighlight>

<code>map()</code> and <code>filter()</code> style operations can be combined into a single array comprehension. Here is one that filters just the even numbers, then creates an array containing their doubles:

<syntaxhighlight lang="javascript">
var numbers = [1, 2, 3, 21, 22, 30];
var doubledEvens = [i * 2 for each (i in numbers) if (i % 2 == 0)];
alert(doubledEvens); // Alerts 4,44,60
</syntaxhighlight>

The square brackets of an array comprehension introduce an implicit block for scoping purposes. New variables (such as i in the example) are treated as if they had been declared using <code>let</code>. This means that they will not be available outside of the comprehension.

The input to an array comprehension does not itself need to be an array; [[/guides/JavaScript/Iterators| iterators and generators]] can also be used.

Even strings may be used as input; to achieve the filter and map actions (under Array-like objects) above:

<syntaxhighlight lang="javascript">
var str = 'abcdef';
var consonantsOnlyStr = [c for each (c in str) if (!(/[aeiouAEIOU]/).test(c))  ].join(''); // 'bcdf'
var interpolatedZeros = [c+'0' for each (c in str) ].join(''); // 'a0b0c0d0e0f0'
</syntaxhighlight>

Again, the input form is not preserved, so we have to use <code>join()</code> to revert back to a string.

==Boolean Object==

The <code>Boolean</code> object is a wrapper around the primitive Boolean data type. Use the following syntax to create a <code>Boolean</code> object:

<syntaxhighlight lang="javascript">
var booleanObjectName = new Boolean(value);
</syntaxhighlight>

Do not confuse the primitive Boolean values <code>true</code> and <code>false</code> with the true and false values of the <code>Boolean</code> object. Any object whose value is not <code>undefined</code>, <code>null</code>, <code>0</code>, <code>NaN</code>, or the empty string , including a <code>Boolean</code> object whose value is false, evaluates to true when passed to a conditional statement. See [[guides/JavaScript/Statements#if...else_Statement|if...else Statement]] for more information.

==Date Object==

JavaScript does not have a date data type. However, you can use the <code>Date</code> object and its methods to work with dates and times in your applications. The <code>Date</code> object has a large number of methods for setting, getting, and manipulating dates. It does not have any properties.

JavaScript handles dates similarly to Java. The two languages have many of the same date methods, and both languages store dates as the number of milliseconds since January 1, 1970, 00:00:00.

The <code>Date</code> object range is -100,000,000 days to 100,000,000 days relative to 01 January, 1970 UTC.

To create a <code>Date</code> object:

<syntaxhighlight lang="javascript">
var dateObjectName = new Date([parameters]);
</syntaxhighlight>

where <code>dateObjectName</code> is the name of the <code>Date</code> object being created; it can be a new object or a property of an existing object.

Calling Date without the new keyword simply converts the provided date to a string representation.

The <code>parameters</code> in the preceding syntax can be any of the following:

* Nothing: creates today's date and time. For example, <code>today = new Date();</code>.
* A string representing a date in the following form: "Month day, year hours:minutes:seconds." For example, <code>var Xmas95 = new Date("December 25, 1995 13:30:00")</code>. If you omit hours, minutes, or seconds, the value will be set to zero.
* A set of integer values for year, month, and day. For example, <code>var Xmas95 = new Date(1995, 11, 25)</code>.
* A set of integer values for year, month, day, hour, minute, and seconds. For example, <code>var Xmas95 = new Date(1995, 11, 25, 9, 30, 0);</code>.

'''JavaScript 1.2 and earlier'''<br /> The <code>Date</code> object behaves as follows:

* Dates prior to 1970 are not allowed.
* JavaScript depends on platform-specific date facilities and behavior; the behavior of the <code>Date</code> object varies from platform to platform.

===Methods of the Date Object===

The <code>Date</code> object methods for handling dates and times fall into these broad categories:

* "set" methods, for setting date and time values in <code>Date</code> objects.
* "get" methods, for getting date and time values from <code>Date</code> objects.
* "to" methods, for returning string values from <code>Date</code> objects.
* parse and UTC methods, for parsing <code>Date</code> strings.

With the "get" and "set" methods you can get and set seconds, minutes, hours, day of the month, day of the week, months, and years separately. There is a <code>getDay</code> method that returns the day of the week, but no corresponding <code>setDay</code> method, because the day of the week is set automatically. These methods use integers to represent these values as follows:

* Seconds and minutes: 0 to 59
* Hours: 0 to 23
* Day: 0 (Sunday) to 6 (Saturday)
* Date: 1 to 31 (day of the month)
* Months: 0 (January) to 11 (December)
* Year: years since 1900

For example, suppose you define the following date:

<syntaxhighlight lang="javascript">
var Xmas95 = new Date("December 25, 1995");
</syntaxhighlight>

Then <code>Xmas95.getMonth()</code> returns 11, and <code>Xmas95.getFullYear()</code> returns 1995.

The <code>getTime</code> and <code>setTime</code> methods are useful for comparing dates. The <code>getTime</code> method returns the number of milliseconds since January 1, 1970, 00:00:00 for a <code>Date</code> object.

For example, the following code displays the number of days left in the current year:

<syntaxhighlight lang="javascript">
var today = new Date();
var endYear = new Date(1995, 11, 31, 23, 59, 59, 999); // Set day and month
endYear.setFullYear(today.getFullYear()); // Set year to this year
var msPerDay = 24 * 60 * 60 * 1000; // Number of milliseconds per day
var daysLeft = (endYear.getTime() - today.getTime()) / msPerDay;
var daysLeft = Math.round(daysLeft); //returns days left in the year
</syntaxhighlight>

This example creates a <code>Date</code> object named <code>today</code> that contains today's date. It then creates a <code>Date</code> object named <code>endYear</code> and sets the year to the current year. Then, using the number of milliseconds per day, it computes the number of days between <code>today</code> and <code>endYear</code>, using <code>getTime</code> and rounding to a whole number of days.

The <code>parse</code> method is useful for assigning values from date strings to existing <code>Date</code> objects. For example, the following code uses <code>parse</code> and <code>setTime</code> to assign a date value to the <code>IPOdate</code> object:

<syntaxhighlight lang="javascript">
var IPOdate = new Date();
IPOdate.setTime(Date.parse("Aug 9, 1995"));
</syntaxhighlight>

===Using the Date Object: an Example===

In the following example, the function <code>JSClock()</code> returns the time in the format of a digital clock.

<syntaxhighlight lang="javascript">
function JSClock() {
  var time = new Date();
  var hour = time.getHours();
  var minute = time.getMinutes();
  var second = time.getSeconds();
  var temp = "" + ((hour > 12) ? hour - 12 : hour);
  if (hour == 0)
    temp = "12";
  temp += ((minute < 10) ? ":0" : ":") + minute;
  temp += ((second < 10) ? ":0" : ":") + second;
  temp += (hour >= 12) ? " P.M." : " A.M.";
  return temp;
 }
</syntaxhighlight>

The <code>JSClock</code> function first creates a new <code>Date</code> object called <code>time</code><nowiki>; since no arguments are given, time is created with the current date and time. Then calls to the </nowiki><code>getHours</code>, <code>getMinutes</code>, and <code>getSeconds</code> methods assign the value of the current hour, minute and seconds to <code>hour</code>, <code>minute</code>, and <code>second</code>.

The next four statements build a string value based on the time. The first statement creates a variable <code>temp</code>, assigning it a value using a conditional expression; if <code>hour</code> is greater than 12, (<code>hour - 12</code>), otherwise simply hour, unless hour is 0, in which case it becomes 12.

The next statement appends a <code>minute</code> value to <code>temp</code>. If the value of <code>minute</code> is less than 10, the conditional expression adds a string with a preceding zero; otherwise it adds a string with a demarcating colon. Then a statement appends a seconds value to <code>temp</code> in the same way.

Finally, a conditional expression appends "PM" to <code>temp</code> if <code>hour</code> is 12 or greater; otherwise, it appends "AM" to <code>temp</code>.

==Function Object==

The predefined <code>Function</code> object specifies a string of JavaScript code to be compiled as a function.

To create a <code>Function</code> object:

<syntaxhighlight lang="javascript">
var functionObjectName = new Function ([arg1, arg2, ... argn], functionBody);
</syntaxhighlight>

<code>functionObjectName</code> is the name of a variable or a property of an existing object. It can also be an object followed by a lowercase event handler name, such as <code>window.onerror</code>.

<code>arg1</code>, <code>arg2</code>, ... <code>argn</code> are arguments to be used by the function as formal argument names. Each must be a string that corresponds to a valid JavaScript identifier; for example "x" or "theForm".

<code>functionBody</code> is a string specifying the JavaScript code to be compiled as the function body.

<code>Function</code> objects are evaluated each time they are used. This is less efficient than declaring a function and calling it within your code, because declared functions are compiled.

In addition to defining functions as described here, you can also use the [[/js/statements/function|<code>function</code> statement]] and the function expression. See the [[/js|JavaScript Reference]] for more information.

The following code assigns a function to the variable <code>setBGColor</code>. This function sets the current document's background color.

<syntaxhighlight lang="javascript">
var setBGColor = new Function("document.bgColor = 'antiquewhite'");
</syntaxhighlight>

To call the <code>Function</code> object, you can specify the variable name as if it were a function. The following code executes the function specified by the <code>setBGColor</code> variable:

<syntaxhighlight lang="javascript">
var colorChoice="antiquewhite";
if (colorChoice=="antiquewhite") {setBGColor()}
</syntaxhighlight>

You can assign the function to an event handler in either of the following ways:

<syntaxhighlight lang="javascript">
document.form1.colorButton.onclick = setBGColor;
</syntaxhighlight>

<syntaxhighlight lang="html5">
<INPUT NAME="colorButton" TYPE="button"
   VALUE="Change background color"
   onClick="setBGColor()">
</syntaxhighlight>

Creating the variable <code>setBGColor</code> shown above is similar to declaring the following function:

<syntaxhighlight lang="javascript">
function setBGColor() {
  document.bgColor = 'antiquewhite';
}
</syntaxhighlight>

Assigning a function to a variable is similar to declaring a function, but there are differences:

* When you assign a function to a variable using <code>var setBGColor = new Function("...")</code>, <code>setBGColor</code> is a variable for which the current value is a reference to the function created with <code>new Function()</code>.
* When you create a function using <code>function setBGColor() {...}</code>, <code>setBGColor</code> is not a variable, it is the name of a function.

You can nest a function within a function. The nested (inner) function is private to its containing (outer) function:

* The inner function can be accessed only from statements in the outer function.
* The inner function can use the arguments and variables of the outer function. The outer function cannot use the arguments and variables of the inner function.

==Math Object==

The predefined <code>Math</code> object has properties and methods for mathematical constants and functions. For example, the <code>Math</code> object's <code>PI</code> property has the value of pi (3.141...), which you would use in an application as

 Math.PI

Similarly, standard mathematical functions are methods of <code>Math</code>. These include trigonometric, logarithmic, exponential, and other functions. For example, if you want to use the trigonometric function sine, you would write

 Math.sin(1.56)

Note that all trigonometric methods of <code>Math</code> take arguments in radians.

The following table summarizes the <code>Math</code> object's methods.

{{{!}} class="standard-table"
{{!}}+  Table 7.1 Methods of Math
{{!}}-
! scope="col" {{!}} Method
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>abs</code>
{{!}} Absolute value
{{!}}-
{{!}} <code>sin</code>, <code>cos</code>, <code>tan</code>
{{!}} Standard trigonometric functions; argument in radians
{{!}}-
{{!}} <code>acos</code>, <code>asin</code>, <code>atan</code>, <code>atan2</code>
{{!}} Inverse trigonometric functions; return values in radians
{{!}}-
{{!}} <code>exp</code>, <code>log</code>
{{!}} Exponential and natural logarithm, base <code>e</code>
{{!}}-
{{!}} <code>ceil</code>
{{!}} Returns least integer greater than or equal to argument
{{!}}-
{{!}} <code>floor</code>
{{!}} Returns greatest integer less than or equal to argument
{{!}}-
{{!}} <code>min</code>, <code>max</code>
{{!}} Returns greater or lesser (respectively) of two arguments
{{!}}-
{{!}} <code>pow</code>
{{!}} Exponential; first argument is base, second is exponent
{{!}}-
{{!}} <code>random</code>
{{!}} Returns a random number between 0 and 1.
{{!}}-
{{!}} <code>round</code>
{{!}} Rounds argument to nearest integer
{{!}}-
{{!}} <code>sqrt</code>
{{!}} Square root
{{!}}}

Unlike many other objects, you never create a <code>Math</code> object of your own. You always use the predefined <code>Math</code> object.

==Number Object==

The <code>Number</code> object has properties for numerical constants, such as maximum value, not-a-number, and infinity. You cannot change the values of these properties and you use them as follows:

<syntaxhighlight lang="javascript">
var biggestNum = Number.MAX_VALUE;
var smallestNum = Number.MIN_VALUE;
var infiniteNum = Number.POSITIVE_INFINITY;
var negInfiniteNum = Number.NEGATIVE_INFINITY;
var notANum = Number.NaN;
</syntaxhighlight>

You always refer to a property of the predefined <code>Number</code> object as shown above, and not as a property of a <code>Number</code> object you create yourself.

The following table summarizes the <code>Number</code> object's properties.

{{{!}} class="standard-table"
{{!}}+  Table 7.2 Properties of Number
{{!}}-
! scope="col" {{!}} Property
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>MAX_VALUE</code>
{{!}} The largest representable number
{{!}}-
{{!}} <code>MIN_VALUE</code>
{{!}} The smallest representable number
{{!}}-
{{!}} <code>NaN</code>
{{!}} Special "not a number" value
{{!}}-
{{!}} <code>NEGATIVE_INFINITY</code>
{{!}} Special negative infinite value; returned on overflow
{{!}}-
{{!}} <code>POSITIVE_INFINITY</code>
{{!}} Special positive infinite value; returned on overflow
{{!}}}

The Number prototype provides methods for retrieving information from Number objects in various formats. The following table summarizes the methods of <code>Number.prototype</code>.

{{{!}} class="fullwidth-table"
{{!}}+  Table 7.3 Methods of Number.prototype
{{!}}-
! scope="col" {{!}} Method
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>toExponential</code>
{{!}} Returns a string representing the number in exponential notation.
{{!}}-
{{!}} <code>toFixed</code>
{{!}} Returns a string representing the number in fixed-point notation.
{{!}}-
{{!}} <code>toPrecision</code>
{{!}} Returns a string representing the number to a specified precision in fixed-point notation.
{{!}}-
{{!}} <code>toSource</code>
{{!}} Returns an object literal representing the specified <code>Number</code> object; you can use this value to create a new object. Overrides the <code>Object.toSource</code> method.
{{!}}-
{{!}} <code>toString</code>
{{!}} Returns a string representing the specified object. Overrides the <code>Object.toString </code>method.
{{!}}-
{{!}} <code>valueOf</code>
{{!}} Returns the primitive value of the specified object. Overrides the <code>Object.valueOf </code>method.
{{!}}}

==RegExp Object==

The <code>RegExp</code> object lets you work with regular expressions. It is described in [[/guides/JavaScript/RegExp|Regular Expressions]].

==String Object==

The <code>String</code> object is a wrapper around the string primitive data type. Do not confuse a string literal with the <code>String</code> object. For example, the following code creates the string literal <code>s1</code> and also the <code>String</code> object <code>s2</code>:

<syntaxhighlight lang="javascript">
var s1 = "foo"; //creates a string literal value
var s2 = new String("foo"); //creates a String object
</syntaxhighlight>

You can call any of the methods of the <code>String</code> object on a string literal value—JavaScript automatically converts the string literal to a temporary <code>String</code> object, calls the method, then discards the temporary <code>String</code> object. You can also use the <code>String.length</code> property with a string literal.

You should use string literals unless you specifically need to use a <code>String</code> object, because <code>String</code> objects can have counterintuitive behavior. For example:

<syntaxhighlight lang="javascript">
var s1 = "2 + 2"; //creates a string literal value
var s2 = new String("2 + 2"); //creates a String object
eval(s1); //returns the number 4
eval(s2); //returns the string "2 + 2"
</syntaxhighlight>

A <code>String</code> object has one property, <code>length</code>, that indicates the number of characters in the string. For example, the following code assigns <code>x</code> the value 13, because "Hello, World!" has 13 characters:

<syntaxhighlight lang="javascript">
var mystring = "Hello, World!";
var x = mystring.length;
</syntaxhighlight>

A <code>String</code> object has two types of methods: those that return a variation on the string itself, such as <code>substring</code> and <code>toUpperCase</code>, and those that return an HTML-formatted version of the string, such as <code>bold</code> and <code>link</code>.

For example, using the previous example, both <code>mystring.toUpperCase()</code> and <code>"hello, world!".toUpperCase()</code> return the string "HELLO, WORLD!"

The <code>substring</code> method takes two arguments and returns a subset of the string between the two arguments. Using the previous example, <code>mystring.substring(4, 9)</code> returns the string "o, Wo". See the [[/js/objects/String/substring|<code>substring</code>]] method of the <code>String</code> object in the JavaScript Reference for more information.

The <code>String</code> object also has a number of methods for automatic HTML formatting, such as <code>bold</code> to create boldface text and <code>link</code> to create a hyperlink. For example, you could create a hyperlink to a hypothetical URL with the <code>link</code> method as follows:

<syntaxhighlight lang="javascript">
mystring.link("http://www.helloworld.com");
</syntaxhighlight>

The following table summarizes the methods of <code>String</code> objects.

{{{!}} class="fullwidth-table"
{{!}}+  Table 7.4 Methods of String Instances
{{!}}-
! scope="col" {{!}} Method
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>[[/js/objects/String/anchor|anchor]]</code>
{{!}} Creates HTML named anchor.
{{!}}-
{{!}} <code>[[/js/objects/String/big|big]]</code>, <code>[[/js/objects/String/blink|blink]]</code>, <code>[[/js/objects/String/bold|bold]]</code>, <code>[[/js/objects/String/fixed|fixed]]</code>, <code>[[/js/objects/String/italics|italics]]</code>, <code>[[/js/objects/String/small|small]]</code>, <code>[[/js/objects/String/strike|strike]]</code>, <code>[[/js/objects/String/sub|sub]]</code>, <code>[[/js/objects/String/sup|sup]]</code>
{{!}} Create HTML formatted string.
{{!}}-
{{!}} <code>[[/js/objects/String/charAt|charAt]]</code>, <code>[[/js/objects/String/charCodeAt|charCodeAt]]</code>
{{!}} Return the character or character code at the specified position in string.
{{!}}-
{{!}} <code>[[/js/objects/String/indexOf|indexOf]]</code>, <code>[[/js/objects/String/lastIndexOf|lastIndexOf]]</code>
{{!}} Return the position of specified substring in the string or last position of specified substring, respectively.
{{!}}-
{{!}} <code>[[/js/objects/String/link|link]]</code>
{{!}} Creates HTML hyperlink.
{{!}}-
{{!}} <code>[[/js/objects/String/concat|concat]]</code>
{{!}} Combines the text of two strings and returns a new string.
{{!}}-
{{!}} <code>[[/js/objects/String/fromCharCode|fromCharCode]]</code>
{{!}} Constructs a string from the specified sequence of Unicode values. This is a method of the String class, not a String instance.
{{!}}-
{{!}} <code>[[/js/objects/String/split|split]]</code>
{{!}} Splits a <code>String</code> object into an array of strings by separating the string into substrings.
{{!}}-
{{!}} <code>[[/js/objects/String/slice|slice]]</code>
{{!}} Extracts a section of an string and returns a new string.
{{!}}-
{{!}} <code>[[/js/objects/String/substring|substring]]</code>, <code>[[/js/objects/String/substr|substr]]</code>
{{!}} Return the specified subset of the string, either by specifying the start and end indexes or the start index and a length.
{{!}}-
{{!}} <code>[[/js/objects/String/match|match]]</code>, <code>[[/js/objects/String/replace|replace]]</code>, <code>[[/js/objects/String/search|search]]</code>
{{!}} Work with regular expressions.
{{!}}-
{{!}} <code>[[/js/objects/String/toLowerCase|toLowerCase]]</code>, <code>[[/js/objects/String/toUpperCase|toUpperCase]]</code>
{{!}} Return the string in all lowercase or all uppercase, respectively.
{{!}}}

<div>

<span style="float: left">[[/guides/JavaScript/Working_with_Objects |&laquo; Previous]]</span>[[/guides/JavaScript/Details_of_the_Object_Model|Next &raquo;]]

</div>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Predefined_Core_Objects
|MSDN_link=
|HTML5Rocks_link=
}}