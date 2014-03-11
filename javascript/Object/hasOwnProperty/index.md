{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Determines whether an object has a property with the specified name.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=hasOwnProperty( proName )
}}
|Values={{JS Syntax Parameter
|Name=proName
|Required=Required
|Description=String value of a property name.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, all String objects share a common split method. The following code will display '''false''' and '''true'''.
|Code=var s = new String("Sample");
 document.write(s.hasOwnProperty("split"));
 document.write("&lt;br/&gt;");
 document.write(String.prototype.hasOwnProperty("split"));
 
 // Output:
 // false
 // true
}}
}}
{{Remarks_Section
|Remarks=The '''hasOwnProperty''' method returns true if object has a property of the specified name, false if it does not. This method does not check the properties in the object's prototype chain; the property must be a member of the object itself.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Array
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/328kyd6z(v=vs.94).aspx
|HTML5Rocks_link=
}}