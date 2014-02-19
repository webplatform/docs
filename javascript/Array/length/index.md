{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Basically specifies the number of elements (AKA length) in an '''Array''' object. This means the '''length''' property represents a number one greater than the largest index defined in an '''Array''' object.

The type of its value must be the unsigned 32 bit integer in the range 0 through 4294967295, inclusive.

The attributes of the '''length''' property are { Writable: true, Enumerable: false, Configurable: false }. So you can set the '''length''' property to extend or truncate an Array object at any time.
}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayObj.length
arrayObj.length = numVar;
}}
|Values={{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=Any Array object.
}}{{JS Syntax Parameter
|Name=numVar
|Required=Required
|Description=Any number less than 2 to the 32nd power.
}}
}}
{{JS_Return_Value
|Description=Any number less than 2 to the 32nd power.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The array classes represents the content list of some training course. They are all displayed in the console by iterating over the array classes.
|Code=var classes = ["HTML", "CSS", "JavaScript"];
document.write("This course includes:<br>");
for (var i = 0, j = classes.length; i < j; i++) {
    document.write(classes[i] + "<br>");
}
// Output: 
// This course includes:
// HTML
// CSS
// JavaScript
|LiveURL=http://code.webplatform.org/gist/9086506
}}{{Single Example
|Language=JavaScript
|Description=This shows how to limit the number of items added into a shopping cart. The length property shortens the array cart to a length of 3 if the current length is larger than 3.
|Code=var cart = ["bread", "cheese", "coffee"];

cart.push("salad"); // length = 4
if (cart.length > 3) {
    alert("Don't add more than 3 items!");
    cart.length = 3;
    document.write(cart);
}

// Output: bread,cheese,coffee
|LiveURL=http://code.webplatform.org/gist/9086602
}}
}}
{{Remarks_Section
|Remarks=In JavaScript arrays are sparse, and the elements in an array do not have to be contiguous. The '''length''' property is not necessarily the number of elements in the array. For example, in the following array definition, <code>my_array.length</code> contains 7, not 2:

 var my_array = new Array( );
 my_array[0] = "Test";
 my_array[6] = "Another Test";
 console.log(my_array.length);
 
 // Output
 // 7
Even if you set length to a number greater than its previous value, the number of actual elements does not increase.

 console.log(my_array.length); // 7
 my_array.length = 10;
 console.log(Object.keys(my_array));
 
 // Output
 // ["0", "6"]
On the other hand, when decreasing length, the array is truncated.

 console.log(my_array.length); // 10
 my_array.length = 1;
 console.log(Object.keys(my_array));
 
 // Output
 // ["0"]
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length JavaScript, by Mozilla Developer Network]
* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Relationship_between_length_and_numerical_properties Relationship between length and numerical properties, by Mozilla Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.5.2 15.4.5.2 length]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Property
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/d8ez24f2(v=vs.94).aspx
|HTML5Rocks_link=
}}