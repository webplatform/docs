{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Executes one or more statements for each property of an object, or each element of an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=for ( variable in [ object {{!}} array ]) {
    statements
}
}}
|Values={{JS Syntax Parameter
|Name=variable
|Required=Required
|Description=A variable that can be any property name of object or any element index of an array.
}}{{JS Syntax Parameter
|Name=object , array
|Required=Optional
|Description=An object or array over which to iterate.
}}{{JS Syntax Parameter
|Name=statements
|Required=Optional
|Description=One or more statements to be executed for each property of object or each element of array. Can be a compound statement.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the for...in statement with an object used as an associative array.
|Code=// Initialize object.
 a = {"a" : "Athens" , "b" : "Belgrade", "c" : "Cairo"}
 
 // Iterate over the properties.
 var s = ""
 for (var key in a) {
     s += key + ": " + a[key];
     s += "&lt;br /&gt;";
 }
 document.write (s);
 
 // Output:
 // a: Athens
 // b: Belgrade
 // c: Cairo
}}{{Single Example
|Language=JavaScript
|Description=This example illustrates the use of the for ... in statement to iterate though an '''Array''' object that has expando properties.
|Code=// Initialize the array.
 var arr = new Array("zero","one","two");
 
 // Add a few expando properties to the array.
 arr["orange"] = "fruit";
 arr["carrot"] = "vegetable";
 
 // Iterate over the properties and elements.
 var s = "";
 for (var key in arr) {
     s += key + ": " + arr[key];
     s += "&lt;br /&gt;";
 }
 
 document.write (s);
 
 // Output:
 //   0: zero
 //   1: one
 //   2: two
 //   orange: fruit
 //   carrot: vegetable
}}
}}
{{Remarks_Section
|Remarks=At the beginning of each iteration of a loop, the value of variable is the next property name of object or the next element index of array. You can then use variable in any of the statements inside the loop to reference the property of object or the element of array.

The properties of an object are not assigned in a determinate manner. You cannot specify a particular property by its index, only by the name of the property.

Iterating through an array is performed in element order, that is, 0, 1, 2.
}}
{{Notes_Section
|Notes=Use the '''Enumerator''' object to iterate over the members of a collection.
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/for{{!}}for Statement]]
* [[javascript/statements/while{{!}}while Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/55wb2d34(v=vs.94).aspx
|HTML5Rocks_link=
}}