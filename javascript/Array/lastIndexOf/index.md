{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns the index of the last occurrence of a specified value in an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=lastIndexOf( searchElement [, fromIndex ])
}}
|Values={{JS Syntax Parameter
|Name=searchElement
|Required=Required
|Description=The value to locate in array1.
}}{{JS Syntax Parameter
|Name=fromIndex
|Required=Optional
|Description=The array index at which to begin the search. If fromIndex is omitted, the search starts at the last index in the array.
}}
}}
{{JS_Return_Value
|Description=The index of the last occurrence of searchElement in the array, or -1 if searchElement is not found.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples illustrate the use of the '''lastIndexOf''' method.
|Code=// Create an array.
 var ar = ["ab", "cd", "ef", "ab", "cd"];
 
 // Determine the first location, in descending order, of "cd".
 document.write(ar.lastIndexOf("cd") + "&lt;br/&gt;");
 
 // Output: 4
 
 // Find "cd" in descending order, starting at index 2.
 document.write(ar.lastIndexOf("cd", 2) + "&lt;br/&gt;");
 
 // Output: 1
 
 // Search for "gh" (which is not found).
 document.write(ar.lastIndexOf("gh")+ "&lt;br/&gt;");
 
 // Output: -1
 
 // Find "ab" with a fromIndex argument of -3.
 // The search in descending order starts at index 3,
 // which is the array length minus 2.
 document.write(ar.lastIndexOf("ab", -3) + "&lt;br/&gt;");
 // Output: 0
}}
}}
{{Remarks_Section
|Remarks=The '''lastIndexOf''' method searches an array for a specified value. The method returns the index of the last occurrence, or -1 if the specified value is not found.

The search occurs in descending index order (last member first). To search in ascending order, use the [[javascript/Array/indexOf{{!}}indexOf Method (Array)]].

The array elements are compared to the searchElement value by strict equality, similar to the comparison made by the === operator. For more information, see [[javascript/operators/comparison{{!}}Comparison Operators]].

The optional fromIndex argument specifies the array index at which to begin the search. If fromIndex is greater than or equal to the array length, the whole array is searched. If fromIndex is negative, the search starts at the array length plus fromIndex. If the computed index is less than 0, -1 is returned.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array/indexOf{{!}}indexOf Method (Array)]]
* [[javascript/Array{{!}}Array Object]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679972(v=vs.94).aspx
|HTML5Rocks_link=
}}