{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Tests for the existence of a property in an object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=result = property in object
}}
|Values={{JS Syntax Parameter
|Name=result
|Required=Required
|Description=Any variable.
}}{{JS Syntax Parameter
|Name=property
|Required=Required
|Description=An expression that evaluates to a string expression.
}}{{JS Syntax Parameter
|Name=object
|Required=Required
|Description=Any object.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''in''' operator:
|Code=// Create an object that has some properties.
 var myObject = new Object();
 myObject.name = "James";
 myObject.age = "22";
 myObject.phone = "555 0234";
 
 if ("phone" in myObject)
    document.write ("property is present");
 else
    document.write ("property is not present");
 
 // Output: property is present
}}
}}
{{Remarks_Section
|Remarks=The '''in''' operator determines whether an object has a property named property. It also determines whether the property is part of the object's prototype chain. For more information about object prototypes, see Prototypes and Prototype Inheritance.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9k25hbz2(v=vs.94).aspx
|HTML5Rocks_link=
}}