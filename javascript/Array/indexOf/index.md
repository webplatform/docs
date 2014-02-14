{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns the index of the first occurrence of a value in an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=array1.indexOf( searchElement [, fromIndex ])
}}
|Values={{JS Syntax Parameter
|Name=array1
|Required=Required
|Description=An array object.
}}{{JS Syntax Parameter
|Name=searchElement
|Required=Required
|Description=The value to locate in array1.
}}{{JS Syntax Parameter
|Name=fromIndex
|Required=Optional
|Description=The array index at which to begin the search. If fromIndex is omitted, the search starts at index 0.
}}
}}
{{JS_Return_Value
|Description=The index of the first occurrence of searchElement in the array, or -1 if searchElement is not found.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples illustrate the use of the '''indexOf''' method.
|Code=// Create an array. (The elements start at index 0.)
 var ar = ["ab", "cd", "ef", "ab", "cd"];
 
 // Determine the first location of "cd".
 document.write(ar.indexOf("cd") + "&lt;br/&gt;");
 
 // Output: 1
 
 // Find "cd" starting at index 2.
 document.write(ar.indexOf("cd", 2) + "&lt;br/&gt;");
 
 // Output: 4
 
 // Find "gh" (which is not found).
 document.write (ar.indexOf("gh")+ "&lt;br/&gt;");
 
 // Output: -1
 
 // Find "ab" with a fromIndex argument of -2.
 // The search starts at index 3, which is the array length plus -2.
 document.write (ar.indexOf("ab", -2) + "&lt;br/&gt;");
 // Output: 3
}}
}}
{{Remarks_Section
|Remarks=The '''indexOf''' method searches an array for a specified value. The method returns the index of the first occurrence, or -1 if the specified value is not found.

The search occurs in ascending index order.

The array elements are compared to the searchElement value by strict equality, similar to the === operator. For more information, see [[javascript/operators/comparison{{!}}Comparison Operators]].

The optional fromIndex argument specifies the array index at which to begin the search. If fromIndex is greater than or equal to the array length, -1 is returned. If fromIndex is negative, the search starts at the array length plus fromIndex.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/methods{{!}}JavaScript Methods]]
* [[javascript/Array{{!}}Array Object]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679977(v=vs.94).aspx
|HTML5Rocks_link=
}}