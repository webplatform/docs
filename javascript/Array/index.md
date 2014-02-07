{{Page_Title}}
{{Flags
|High-level issues=Unreviewed Import
|Checked_Out=No
}}
{{Summary_Section|Provides support for creation of arrays of any data type.

Array is an object used to list values together. When you create an array, you’re setting up a list that you can fill with key:value pairs. You can then refer to a whole list using just that one array name. You can also refer to one item in the list using the key, also called an index when the key is a number.
|Provides support for creation of arrays of any data type_

Array is an object used to list values together_ When you create an array, you’re setting up a list that you can fill with key:value pairs_ You can then refer to a whole list using just that one array name_ You can also refer to one item in the list using the key, also called an index when the key is a number_
Array is a standard, built-in object_ Among other things, this means you can create a new array by using the object creation expression new Array(), as in:
var myArray=new Array();
But a more efficient way is to use what’s called the literal notation. An array literal is created without using the new keyword. Instead, you use the square brackets [] and list out what should be in the array:
var myAnimals = ["cat", "dog", "rabbit"];
Using an array literal to declare your array this way avoids some of the quirkiness of the creation expression new Array(). (For more information, see Stoyan Stefanov's JavaScript Patterns.)
Your array can consist of different values and types. Here's an array that provides describes my dog:
var goodDog = ["Rover", 7, true];
This array combines a string, a number and a Boolean value.
An array is often called a zero-indexed, or zero-based index, because the numerical key, or index, starts at zero. (prof.dr. Edsger W. Dijkstra gives a reason why numbering should start at zero.) This means you can refer to the items in your array by referencing the index. So in goodDog, above, you reference the dog's name with goodDog[0], or his age with goodDog[1], or whether he is, indeed, a good dog with goodDog[3].
Arrays can be dimensional as well. This helps when your setting up something that has row and column patterns, such as seats in a theatre or a checkerboard. So, for example, to describe a college dormitory that has 5 beds per floor and 2 floors, you can set up a two-dimensional array that looks like the following:

var dorm = [[1,1], [1,2], [1,3], [1,4], [1,5], 
            [2,1], [2,2], [2,3], [2,4], [2,5]];
Arrays are a useful kind of object for many reasons. For example, because the keys are numerical indexes by default, it's easy to iterate, or loop, through all of the values. They also have special properties that other objects don't have.
}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=[ element0 [, element1 [, ...[, elementN ]]]]
}}{{JS Syntax Format
|Format=new Array([ element0 [, element1 [, ...[, elementN ]]]])
}}{{JS Syntax Format
|Format=new Array([ len ])
}}
|Values={{JS Syntax Parameter
|Name=element0,...,elementN
|Required=Optional
|Description=The elements to place in the array. This creates an array with n + 1 elements, and a '''length''' of n + 1. Using this syntax, you must supply more than one element.
}}{{JS Syntax Parameter
|Name=length
|Required=Optional
|Description=The length of the array. As arrays are zero-based, created elements will have indexes from zero to size -1.
}}
}}
{{JS_Return_Value
|Description=When no arguments are provided, creates and returns a new Array object, with a length property (whose initial value is +0).

When multiple arguments are provided, creates and returns a new Array object with the elements provided, with a length property the number of arguments + 1.

And if only one Number is provided as the argument, with argument len is a Number and ToUint32(len) (an unsigned 32-bit integer), then the length property of the newly constructed object is set to ToUint32(len).

If the only argument is a Number and ToUint32(len) is not equal to len, a RangeError exception is thrown.

If the only argument is not a Number, then the length property of the newly constructed object is set to 1 and the 0 property of the newly constructed object is set to len.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=After an array is created, you can access the individual elements of the array by using [n] notation. Note that unlike other programming languages, arrays keys are only numeric. Keys starts by 0.
|Code=// Literal notation
var my_array = [];
 for (i = 0; i &lt; 10; i++) {
     my_array[i] = i;
 }
 x = my_array[4];
console.log(x);
 
// Output: 4
|LiveURL=http://code.webplatform.org/gist/8856397
}}{{Single Example
|Language=JavaScript
|Description=You can pass an unsigned 32-bit integer to the '''Array''' constructor to specify the size of the array. If the value is negative or not an integer, a run-time error occurs. If you run the following code, you should see this error in the Console.
|Code=var arr = new Array(10);
document.write(arr.length);
// Output: 10
 
// Don't do this
var arr = new Array(-1);
arr = new Array(1.50);
|LiveURL=http://code.webplatform.org/gist/8856471
}}{{Single Example
|Language=JavaScript
|Description=If a single value is passed to the '''Array''' constructor, and it is not a number, the '''length''' property is set to 1, and the value of the only element becomes the single, passed-in argument.
|Code=var arr = new Array("one");
 document.write(arr.length);
 document.write(arr[0]);
 
 // Output:
 // 1
 // one
|LiveURL=http://code.webplatform.org/gist/8856494
}}{{Single Example
|Language=JavaScript
|Description=Adding members, to an array can be done by using the prototypal inheritance chain and call the <code>push()</code> method on it.
|Code=var ponies = ['Twilight Sparkle','Pinkie Pie','Rainbow Dash'];

// Adding a new member
ponies.push('Spike');
console.log(ponies[3]);

// Output:
// Spike
|LiveURL=http://code.webplatform.org/gist/8857418
}}
}}
{{Remarks_Section
|Remarks=JavaScript arrays are referred to as "sparse," which means that elements in an array can be undefined and deleted. The keys, or index, are not reordered into a denser table, unless you do so, explicitly.
}}
{{Notes_Section
|Usage=Array is a standard, built-in object. Among other things, this means you can create a new array by using the object creation expression <code>new Array()</code>, as in:
<pre>var myArray = new Array();</pre>

But a more efficient way is to use what’s called the literal notation. An array literal is created without using the new keyword. Instead, you use the square brackets <code>[]</code> and list out what should be in the array:

<pre>var myAnimals = ["cat", "dog", "rabbit"];</pre>
Using an array literal to declare your array this way avoids some of the quirkiness of the creation expression <code>new Array()</code>. (For more information, see Stoyan Stefanov's JavaScript Patterns.)
Your array can consist of different values and types. Here's an array that provides describes my dog:
<pre>var goodDog = ["Rover", 7, true];</pre>
This array combines a string, a number and a Boolean value.
An array is often called a zero-indexed, or as having a zero-based index, because the numerical key, or index, starts at zero. (prof.dr. Edsger W. Dijkstra gives a reason why numbering should start at zero.) This means you can refer to the items in your array by referencing the index. So in <code>goodDog</code>, above, you reference the dog's name with <code>goodDog[0]</code>, or his age with <code>goodDog[1]</code>, or whether he is, indeed, a good dog with <code>goodDog[3]</code>.
Arrays can be dimensional as well. This helps when your setting up something that has row and column patterns, such as seats in a theatre or a checkerboard. So, for example, to describe a college dormitory that has 5 beds per floor and 2 floors, you can set up a two-dimensional array that looks like the following:

<pre>
var dorm = [[1,1], [1,2], [1,3], [1,4], [1,5], 
            [2,1], [2,2], [2,3], [2,4], [2,5]];
</pre>

Arrays are a useful kind of object for many reasons. For example, because the keys are numerical indexes by default, it's easy to iterate, or loop, through all of the values. They also have special properties that other objects don't have. But if your array becomes more complex, you may want to consider using an object instead.
}}
==Properties==
The following table lists the properties of the '''Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Array/constructor|constructor Property]]
| Specifies the function that creates an array.
|-
| [[javascript/Array/length|length Property (Array)]]
| Returns an integer value that is one higher than the highest element defined in an array.
|-
| [[javascript/Array/prototype|prototype Property]]
| Returns a reference to the prototype for an array.
|}
==Functions==
The following table describes the functions of the '''Array''' object.

{| class='wikitable'
|-
! Function
! Description
|-
| [[javascript/Array/isArray|Array.isArray Function]]
| Returns a Boolean value that indicates whether an object is an array.
|}
==Methods==
The following table lists the methods of the '''Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Array/concat|concat Method (Array)]]
| Returns a new array consisting of a combination of two arrays.
|-
| [[javascript/Array/every|every Method]]
| Checks whether a defined callback function returns true for all elements in an array.
|-
| [[javascript/Array/filter|filter Method]]
| Calls a defined callback function on each element of an array, and returns an array of values for which the callback function returns true.
|-
| [[javascript/Array/forEach|forEach Method]]
| Calls a defined callback function for each element in an array.
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty Method]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/Array/indexOf|indexOf Method (Array)]]
| Returns the index of the first occurrence of a value in an array.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf Method]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype chain.
|-
| [[javascript/Array/join|join Method]]
| Returns a String object consisting of all the elements of an array concatenated together.
|-
| [[javascript/Array/lastIndexOf|lastIndexOf Method (Array)]]
| Returns the index of the last occurrence of a specified value in an array.
|-
| [[javascript/Array/map|map Method]]
| Calls a defined callback function on each element of an array, and returns an array that contains the results.
|-
| [[javascript/Array/pop|pop Method]]
| Removes the last element from an array and returns it.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable Method]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/Array/push|push Method]]
| Appends new elements to an array, and returns the new length of the array.
|-
| [[javascript/Array/reduce|reduce Method]]
| Accumulates a single result by calling a defined callback function for all elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.
|-
| [[javascript/Array/reduceRight|reduceRight Method]]
| Accumulates a single result by calling a defined callback function for all elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.
|-
| [[javascript/Array/reverse|reverse Method]]
| Returns an '''Array''' object with the elements reversed.
|-
| [[javascript/Array/shift|shift Method]]
| Removes the first element from an array and returns it.
|-
| [[javascript/Array/slice|slice Method (Array)]]
| Returns a section of an array.
|-
| [[javascript/Array/some|some Method]]
| Checks whether a defined callback function returns true for any element of an array.
|-
| [[javascript/Array/sort|sort Method]]
| Returns an '''Array''' object with the elements sorted.
|-
| [[javascript/Array/splice|splice Method]]
| Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.
|-
| [[javascript/Object/toLocaleString|toLocaleString Method]]
| Returns a string using the current locale.
|-
| [[javascript/Array/toString|toString Method]]
| Returns a string representation of an array.
|-
| [[javascript/Array/unshift|unshift Method]]
| Inserts new elements at the start of an array.
|-
| [[javascript/Array/valueOf|valueOf Method]]
| Gets a reference to the array.
|}
{{See_Also_Section
|External_links===Specification==
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4 15.4 Array Objects]

ECMAScript® Language Specification

Standard ECMA-262

5.1 Edition / June 2011
==Recommended links==
[https://developer.mozilla.org/en-US/docs/Web/JavaScript JavaScript, by Mozilla Developer Network]

[http://eloquentjavascript.net/ Eloquent JavaScript: A Modern Introduction to Programming, by Marijn Haverbeke]

[http://tddjs.com/ Test-Driven JavaScript Development]

[http://shop.oreilly.com/product/9780596806767.do JavaScript Patterns: Build Better Applications with Coding and Design Patterns, By Stoyan Stefanov] 

[http://www.manning.com/resig/ Secrets of the JavaScript Ninja, by John Resig and Bear Bibeault]


}}
{{Topics|JS Basic}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/k4h76zbx(v=vs.94).aspx
|HTML5Rocks_link=
}}