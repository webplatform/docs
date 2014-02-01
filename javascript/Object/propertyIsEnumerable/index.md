{{Page_Title}}
{{Flags}}
{{Summary_Section|Determines whether a specified property is enumerable.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= object. propertyIsEnumerable( proName )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=Instance of an object.}}{{JS_Syntax_Parameter
|Name=proName
|Required=Required
|Description=String value of a property name.}}
}}
{{Remarks_Section
|Remarks=The '''propertyIsEnumerable''' method returns true if proName exists in object and can be enumerated using a For loop. The '''propertyIsEnumerable''' method returns false if object does not have a property of the specified name or if the specified property is not enumerable. Typically, predefined properties are not enumerable, but user-defined properties are always enumerable.

The '''propertyIsEnumerable''' method does not consider objects in the prototype chain.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Code= var a = new Array("apple", "banana", "cactus");
 document.write(a.propertyIsEnumerable(1));
 
 // Output: true
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/prototype{{!}}prototype Property (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/adebfyya(v=vs.94).aspx
|HTML5Rocks_link=
}}