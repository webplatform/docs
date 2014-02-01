{{Page_Title}}
{{Flags}}
{{Summary_Section|Tests for the existence of a property in an object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= result = property in object}}
|Values={{JS_Syntax_Parameter
|Name=result
|Required=Required
|Description=Any variable.}}{{JS_Syntax_Parameter
|Name=property
|Required=Required
|Description=An expression that evaluates to a string expression.}}{{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=Any object.}}
}}
{{Remarks_Section
|Remarks=The '''in''' operator determines whether an object has a property named property. It also determines whether the property is part of the object's prototype chain. For more information about object prototypes, see Prototypes and Prototype Inheritance.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''in''' operator:

|Code= // Create an object that has some properties.
 var myObject = new Object();
 myObject.name = "James";
 myObject.age = "22";
 myObject.phone = "555 0234";
 
 if ("phone" in myObject)
    document.write ("property is present");
 else
    document.write ("property is not present");
 
 // Output: property is present
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9k25hbz2(v=vs.94).aspx
|HTML5Rocks_link=
}}