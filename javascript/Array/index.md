---
title: Array
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/k4h76zbx(v=vs.94).aspx)'
code_samples:
  - 'http://gist.github.com/42267d4185785ffcf82e'
  - 'http://gist.github.com/8856471'
  - 'http://gist.github.com/8856494'
  - 'http://gist.github.com/8857418'
readiness: 'Ready to Use'
summary: "Provides support for creation of arrays of any data type.\n"
tags:
  0: JS
  1: Basic
  3: Object
uri: javascript/Array

---
## Summary

Provides support for creation of arrays of any data type.

Array is an object used to list values together. When you create an array, you’re setting up a list that you can fill with key:value pairs. You can then refer to a whole list using just that one array name. You can also refer to one item in the list using the key, also called an index when the key is a number.

## Syntax

<span class="language">JavaScript</span>

    [ element0 [, element1 [, ...[, elementN ]]]]

<span class="language">JavaScript</span>

    new Array([ element0 [, element1 [, ...[, elementN ]]]])

<span class="language">JavaScript</span>

    new Array([ length ])

**element0,...,elementN**
:   Optional. The elements to place in the array. This creates an array with n + 1 elements, and a **length** of n + 1. Using this syntax, you must supply more than one element.

**length**
:   Optional. The length of the array. As arrays are zero-based, created elements will have indexes from zero to size -1.

## Return Value

When no arguments are provided, creates and returns a new Array object, with a length property (whose initial value is +0).

When multiple arguments are provided, creates and returns a new Array object with the elements provided, with a length property the number of arguments + 1.

And if only one Number is provided as the argument, with argument len is a Number and ToUint32(len) (an unsigned 32-bit integer), then the length property of the newly constructed object is set to ToUint32(len).

If the only argument is a Number and ToUint32(len) is not equal to len, a RangeError exception is thrown.

If the only argument is not a Number, then the length property of the newly constructed object is set to 1 and the 0 property of the newly constructed object is set to len.

## Examples

After an array is created, you can access the individual elements of the array by using [n] notation. Note that unlike other programming languages, arrays keys are only numeric. Keys starts by 0.

``` js
// Literal notation
var my_array = [];
for (i = 0; i < 10; i++) {
  my_array[i] = i;
}
x = my_array[4];
document.write(x);
// Output: 4
```

[View live example](http://code.webplatform.org/gist/42267d4185785ffcf82e)

You can pass an unsigned 32-bit integer to the **Array** constructor to specify the size of the array. If the value is negative or not an integer, a run-time error occurs. If you run the following code, you should see this error in the Console.

``` js
var arr = new Array(10);
document.write(arr.length);
// Output: 10

// Don't do this
var arr = new Array(-1);
arr = new Array(1.50);
```

[View live example](http://code.webplatform.org/gist/8856471)

If a single value is passed to the **Array** constructor, and it is not a number, the **length** property is set to 1, and the value of the only element becomes the single, passed-in argument.

``` js
var arr = new Array("one");
 document.write(arr.length);
 document.write(arr[0]);

 // Output:
 // 1
 // one
```

[View live example](http://code.webplatform.org/gist/8856494)

Adding members, to an array can be done by using the prototypal inheritance chain and call the `push()` method on it.

``` js
var ponies = ['Twilight Sparkle','Pinkie Pie','Rainbow Dash'];

// Adding a new member
ponies.push('Spike');
console.log(ponies[3]);

// Output:
// Spike
```

[View live example](http://code.webplatform.org/gist/8857418)

## Remarks

JavaScript arrays are referred to as "sparse," which means that elements in an array can be undefined and deleted. The keys, or index, are not reordered into a denser table, unless you do so, explicitly.

## Usage

     Array is a standard, built-in object. Among other things, this means you can create a new array by using the object creation expression new Array(), as in:

    var myArray = new Array();

But a more efficient way is to use what’s called the literal notation. An array literal is created without using the `new` keyword. Instead, you use the square brackets `[]` and list out what should be in the array:

    var myAnimals = ["cat", "dog", "rabbit"];

Using an array literal to declare your array this way avoids some of the quirkiness of the creation expression `new Array()`. (For more information, see Stoyan Stefanov's [JavaScript Patterns](http://shop.oreilly.com/product/9780596806767.do).) Your array can consist of different values and types. Here's an array that provides describes my dog:

    var goodDog = ["Rover", 7, true];

This array combines a string, a number and a Boolean value. An array is often called a zero-indexed, or as having a zero-based index, because the numerical key, or index, starts at zero. (prof.dr. Edsger W. Dijkstra gives a reason [why numbering should start at zero](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD08xx/EWD831.html).) This means you can refer to the items in your array by referencing the index. So in `goodDog`, above, you reference the dog's name with `goodDog[0]`, or his age with `goodDog[1]`, or whether he is, indeed, a good dog with `goodDog[2]`. Arrays can be dimensional as well. This helps when your setting up something that has row and column patterns, such as seats in a theatre or a checkerboard. So, for example, to describe a college dormitory that has 5 beds per floor and 2 floors, you can set up a two-dimensional array that looks like the following:

    var dorm = [[1,1], [1,2], [1,3], [1,4], [1,5],
                [2,1], [2,2], [2,3], [2,4], [2,5]];

Arrays are a useful kind of object for many reasons. For example, because the keys are numerical indexes by default, it's easy to iterate, or loop, through all of the values. They also have special properties that other objects don't have. But if your array becomes more complex, you may want to consider using an object instead.

## Properties

The following table lists the properties of the **Array** object.

|Property|Summary|
|:-------|:------|
|[constructor](/javascript/Array/constructor)|References the function which created the instance of the Array object.|
|[length](/javascript/Array/length)|Basically specifies the number of elements (AKA length) in an **Array** object. This means the **length** property represents a number one greater than the largest index defined in an **Array** object.|
|[prototype](/javascript/Array/prototype)|Returns a reference to the prototype for a class of array.|

## Functions

The following table lists the functions of the **Array** object.

## Methods

The following table lists the methods of the **Array** object.

|Method|Summary|
|:-----|:------|
|[concat](/javascript/Array/concat)|Combines two or more arrays.|
|[every](/javascript/Array/every)|Determines whether all the members of an array satisfy the specified test.|
|[filter](/javascript/Array/filter)|Returns the elements of an array that meet the condition specified in a callback function.|
|[forEach](/javascript/Array/forEach)|Performs the specified action for each element in an array.|
|[indexOf](/javascript/Array/indexOf)|Returns the index of the first occurrence of a value in an array.|
|[isArray](/javascript/Array/isArray)|Determines whether an object is an array.|
|[join](/javascript/Array/join)|Adds all the elements of an array separated by the specified separator string.|
|[lastIndexOf](/javascript/Array/lastIndexOf)|Returns the index of the last occurrence of a specified value in an array.|
|[map](/javascript/Array/map)|Calls a defined callback function on each element of an array, and returns an array that contains the results.|
|[pop](/javascript/Array/pop)|Removes the last element from an array and returns it.|
|[push](/javascript/Array/push)|Appends new elements to an array, and returns the new length of the array.|
|[reduce](/javascript/Array/reduce)|Calls the specified callback function for all the elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.|
|[reduceRight](/javascript/Array/reduceRight)|Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.|
|[reverse](/javascript/Array/reverse)|Reverses the elements in an **Array**.|
|[shift](/javascript/Array/shift)|Removes the first element from an array and returns it.|
|[slice](/javascript/Array/slice)|Returns a section of an array.|
|[some](/javascript/Array/some)|Determines whether the specified callback function returns true for any element of an array.|
|[sort](/javascript/Array/sort)|Sorts an **Array**.|
|[splice](/javascript/Array/splice)|Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.|
|[toString](/javascript/Array/toString)|Returns a string representation of an array.|
|[unshift](/javascript/Array/unshift)|Inserts new elements at the start of an array.|
|[valueOf](/javascript/Array/valueOf)|Returns the primitive value of the specified object.|
|[hasOwnProperty](/javascript/Object/hasOwnProperty)|Determines whether an object has a property with the specified name.|
|[isPrototypeOf](/javascript/Object/isPrototypeOf)|Determines whether an object exists in another object's prototype chain.|
|[propertyIsEnumerable](/javascript/Object/propertyIsEnumerable)|Determines whether a specified property is enumerable.|
|[toLocaleString](/javascript/Object/toLocaleString)|Returns a date converted to a string using the current locale.|

## See also

### External resources

-   [JavaScript, by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
-   [Eloquent JavaScript: A Modern Introduction to Programming, by Marijn Haverbeke](http://eloquentjavascript.net/)
-   [Test-Driven JavaScript Development](http://tddjs.com/)
-   [JavaScript Patterns: Build Better Applications with Coding and Design Patterns, By Stoyan Stefanov](http://shop.oreilly.com/product/9780596806767.do)
-   [Secrets of the JavaScript Ninja, by John Resig and Bear Bibeault](http://www.manning.com/resig/)

### Specification

[15.4 Array Objects](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

