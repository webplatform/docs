{{Page_Title}}
{{Flags}}
{{Summary_Section|Deletes a property from an object, or removes an element from an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= delete expression}}
}}
{{Remarks_Section
|Remarks=The expression argument is a valid JavaScript expression that usually results in a property name or array element.

If the result of expression is an object, the property specified in expression exists, and the object will not allow it to be deleted, false is returned.

In all other cases, true is returned.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to remove an element from an array.

|Code= // Create an array.
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
}}{{Single_Example
|Language=JavaScript
|Description=The following example shows how to delete properties from an object.

|Code= // Create an object and add expando properties.
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
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/2b2z052x(v=vs.94).aspx
|HTML5Rocks_link=
}}