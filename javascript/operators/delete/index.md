{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Deletes a property from an object, or removes an element from an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=delete expression
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to remove an element from an array.
|Code=// Create an array.
 var ar = new Array (10, 11, 12, 13, 14);
 
 // Remove an element from the array.
 delete ar[1];
 
 // Print the results.
 document.write ("element 1: " + ar[1]);
 document.write ("&lt;br /&gt;");
 document.write ("array: " + ar);
 // Output:
 //  element 1: undefined
 //  array: 10,,12,13,14
}}{{Single Example
|Language=JavaScript
|Description=The following example shows how to delete properties from an object.
|Code=// Create an object and add expando properties.
 var myObj = new Object();
 myObj.name = "Fred";
 myObj.count = 42;
 
 // Delete the properties from the object.
 delete myObj.name;
 delete myObj["count"];
 
 // Print the results.
 document.write ("name: " + myObj.name);
 document.write ("&lt;br /&gt;");
 document.write ("count: " + myObj.count);
 // Output:
 //  name: undefined
 //  count: undefined
}}
}}
{{Remarks_Section
|Remarks=The expression argument is a valid JavaScript expression that usually results in a property name or array element.

If the result of expression is an object, the property specified in expression exists, and the object will not allow it to be deleted, false is returned.

In all other cases, true is returned.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/2b2z052x(v=vs.94).aspx
|HTML5Rocks_link=
}}