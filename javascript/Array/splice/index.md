{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=splice( start, deleteCount,  [ item1 [, item2 [, . . . [, itemN ]]]])
}}
|Values={{JS Syntax Parameter
|Name=start
|Required=Required
|Description=The zero-based location in the array from which to start removing elements.
}}{{JS Syntax Parameter
|Name=deleteCount
|Required=Required
|Description=The number of elements to remove.
}}{{JS Syntax Parameter
|Name=item1, item2,. . ., itemN
|Required=Optional
|Description=Elements to insert into the array in place of the deleted elements.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use the '''splice''' method.
|Code=var arr = new Array("4", "11", "2", "10", "3", "1");
 arr.splice(2, 2, "21", "31");
 document.write(arr);
 
 // Output: 4,11,21,31,3,1
}}
}}
{{Remarks_Section
|Remarks=The '''splice''' method modifies arrayObj by removing the specified number of elements from position start and inserting new elements. The deleted elements are returned as a new '''Array''' object.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.12 15.4.4.12 Array.prototype.splice (start, deleteCount [ , item1 [ , item2 [ , … ] ] ] )]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wctc5k7s(v=vs.94).aspx
|HTML5Rocks_link=
}}