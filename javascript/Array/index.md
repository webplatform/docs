{{Page_Title}}
{{Flags}}
{{Summary_Section|Provides support for creation of arrays of any data type.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= arrayObj = new Array()}}{{JS_Syntax_Format
|Format= arrayObj = new Array([ size ])}}{{JS_Syntax_Format
|Format= arrayObj = new Array([ element0 [, element1 [, ...[, elementN ]]]])}}
|Values={{JS_Syntax_Parameter
|Name=arrayObj
|Required=Required
|Description=The variable name to which the '''Array''' object is assigned.}}{{JS_Syntax_Parameter
|Name=size
|Required=Optional
|Description=The size of the array. As arrays are zero-based, created elements will have indexes from zero to size -1.}}{{JS_Syntax_Parameter
|Name=element0,...,elementN
|Required=Optional
|Description=The elements to place in the array. This creates an array with n + 1 elements, and a '''length''' of n + 1. Using this syntax, you must supply more than one element.}}
}}
{{Remarks_Section
|Remarks=After an array is created, you can access the individual elements of the array by using [ ] notation. Note that arrays in JavaScript are zero-based.

 var my_array = new Array();
 for (i = 0; i &lt; 10; i++) {
     my_array[i] = i;
 }
 x = my_array[4];
 document.write(x);
 
 // Output: 4
You can pass an unsigned 32-bit integer to the '''Array''' constructor to specify the size of the array. If the value is negative or not an integer, a run-time error occurs. If you run the following code, you should see this error in the Console.

 var arr = new Array(10);
 document.write(arr.length
 
 // Output: 10
 
 // Don't do this
 var arr = new Array(-1);
 arr = new Array(1.50);
If a single value is passed to the '''Array''' constructor, and it is not a number, the '''length''' property is set to 1, and the value of the only element becomes the single, passed-in argument.

 var arr = new Array("one");
 document.write(arr.length);
 document.write("&lt;br/&gt;");
 document.write(arr[0]);
 
 // Output:
 1
 one
JavaScript arrays are sparse arrays, which means that not all the elements in an array may contain data. In JavaScript, only the elements that actually contain data exist in the array. This reduces the amount of memory used by the array.
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
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/k4h76zbx(v=vs.94).aspx
|HTML5Rocks_link=
}}