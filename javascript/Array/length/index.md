{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Basically specifies the number of elements (AKA length) in an Array object. This means the length property represents a number one greater than the largest index defined in an Array object.

The type of its value must be the unsigned 32 bit integer in the range 0 through 4294967295, inclusive.

The attributes of the length property are { [[Writable]]: true, [[Enumerable]]: false, [[Configurable]]: false }. So you can set the length property to extend or truncate an Array object at any time.
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
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Manual_links=[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length JavaScript, by Mozilla Developer Network]
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Relationship_between_length_and_numerical_properties Relationship between length and numerical properties, by Mozilla Developer Network]
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