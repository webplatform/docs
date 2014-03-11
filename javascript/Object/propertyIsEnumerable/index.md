{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Determines whether a specified property is enumerable.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=propertyIsEnumerable( proName )
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
|Code=var a = new Array("apple", "banana", "cactus");
 document.write(a.propertyIsEnumerable(1));
 
 // Output: true
}}
}}
{{Remarks_Section
|Remarks=The '''propertyIsEnumerable''' method returns true if proName exists in object and can be enumerated using a For loop. The '''propertyIsEnumerable''' method returns false if object does not have a property of the specified name or if the specified property is not enumerable. Typically, predefined properties are not enumerable, but user-defined properties are always enumerable.

The '''propertyIsEnumerable''' method does not consider objects in the prototype chain.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Object/prototype{{!}}prototype Property (Object)]]
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Array
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/adebfyya(v=vs.94).aspx
|HTML5Rocks_link=
}}