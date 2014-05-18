{{Page_Title}}
{{Flags
|High-level issues=Needs Topics
|Checked_Out=Yes
}}
{{Summary_Section|An object that represents a number of any kind. All JavaScript numbers are 64-bit floating-point numbers.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=new Number( value )
}}
|Values={{JS Syntax Parameter
|Name=value
|Required=Required
|Description=The numeric value.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// Returns an Object
var thousand = new Number(1000);
console.log(thousand.valueOf() === 1000);
}}{{Single Example
|Language=JavaScript
|Code=// Returns an Object
var googol = new Number(1e+100);
console.log(googol.valueOf() === 1e+100);
}}{{Single Example
|Language=JavaScript
|Code=// Alfred B. Taylor octal notation for the decimal number 10
untydu = new Number(012);
console.log(untydu.valueOf() === 10);
}}
}}
{{Remarks_Section
|Remarks=JavaScript creates '''Number''' objects when a variable is set to a number value, for example <code>var num = 255.336;</code>. It is seldom necessary to create '''Number''' objects explicitly.

The '''Number''' object has its own properties and methods, in addition to the properties and methods inherited from '''Object'''. Numbers are converted into strings under certain circumstances, for example when a number is added or concatenated with a string, as well as by means of the '''toString''' method. For more information, see [[javascript/operators/addition{{!}}Addition Operator (+)]].

JavaScript has several number constants. For a complete list, see [[javascript/Number/constants{{!}}Number Constants]].

'''The Number Type.'''

The Number type has exactly 18437736874454810627 (that is, 264−253+3) values, representing the double-precision 64-bit format IEEE 754 values as specified in the IEEE Standard for Binary Floating-Point Arithmetic, except that the 9007199254740990 (that is, 253−2) distinct “Not-a-Number” values of the IEEE Standard are represented in ECMAScript as a single special [[javascript/NaN{{!}}JavaScript NaN constant]] value.
}}
{{Notes_Section
|Notes='''Octals and Hexadecimals'''

Octal and hexadecimal numbers can be used in JavaScript.

Octal numbers must begin with 0 (zero) followed by one or more octal digits.

Hexadecimal numbers must begin with 0x.
}}
{{JS Object Listing}}
==Properties==
The following table lists the properties of the '''Number''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Object/constructor|constructor Property]]
| Specifies the function that creates an object.
|-
| [[javascript/Object/prototype|prototype Property]]
| Returns a reference to the prototype for a class of objects.
|}
==Methods==
The following table lists the methods of the '''Number''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty Method]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf Method]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype hierarchy.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable Method]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/Number/toExponential|toExponential method]]
| Returns a string that contains a number represented in exponential notation.
|-
| [[javascript/Number/toFixed|toFixed method]]
| Returns a string that represents a number in fixed-point notation.
|-
| [[javascript/Object/toLocaleString|toLocaleString Method]]
| Returns an object converted to a string based on the current locale.
|-
| [[javascript/Number/toPrecision|toPrecision method]]
| Returns a string that contains a number that is represented in either exponential or fixed-point notation and that has a specified number of digits.
|-
| [[javascript/Object/toString|toString Method]]
| Returns a string representation of an object.
|-
| [[javascript/Object/valueOf|valueOf Method]]
| Returns the primitive value of the specified object.
|}

{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/objects{{!}}JavaScript Objects]]
* [[javascript/Math{{!}}Math Object]]
* [[javascript/operators/new{{!}}new Operator]]
* [[javascript/NaN{{!}}JavaScript NaN constant]]
|External_links=* http://www.ecma-international.org/ecma-262/5.1/#sec-8.5
* http://en.wikipedia.org/wiki/Octal
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dwab3ed2(v=vs.94).aspx
|HTML5Rocks_link=
}}