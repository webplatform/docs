{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Sorts an '''Array'''.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayobj.sort( sortFunction )
}}
|Values={{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=Any '''Array''' object.
}}{{JS Syntax Parameter
|Name=sortFunction
|Required=Optional
|Description=The name of the function used to determine the order of the elements. If omitted, the elements are sorted in ascending, ASCII character order.
}}
}}
{{JS_Return_Value
|Description=The sorted array.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''sort''' method.
|Code=var a = new Array(4, 11, 2, 10, 3, 1);
 
 var b = a.sort();
 document.write(b);
 document.write("&lt;br/&gt;");
 
 // This is ASCII character order.
 // Output: 1,10,11,2,3,4)
 
 // Sort the array elements with a function that compares array elements.
 b = a.sort(CompareForSort);
 document.write(b);
 document.write("&lt;br/&gt;");
 // Output: 1,2,3,4,10,11.
 
 // Sorts array elements in ascending order numerically.
 function CompareForSort(first, second)
 {
     if (first == second)
         return 0;
     if (first &lt; second)
         return -1;
     else
         return 1; 
 }
}}
}}
{{Remarks_Section
|Remarks=The '''sort''' method sorts the '''Array''' object in place; no new '''Array''' object is created during execution.

If you supply a function in the sortFunction argument, it must return one of the following values:

* A negative value if the first argument passed is less than the second argument.
* Zero if the two arguments are equivalent.
* A positive value if the first argument is greater than the second argument.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/4b4fbfhk(v=vs.94).aspx
|HTML5Rocks_link=
}}