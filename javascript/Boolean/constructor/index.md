{{Page_Title}}
{{Flags
|State=In Progress
|Checked_Out=No
}}
{{Summary_Section|Initializes a Boolean object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=boolean.constructor([ value ])
}}
|Values={{JS Syntax Parameter
|Name=boolean
|Required=Required
|Description=The name of the Boolean object being created
}}{{JS Syntax Parameter
|Name=value
|Required=Optional
|Description=Specifies the value of the Boolean object. This can be the numbers 1 or 0, or the strings "true" or "false".
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.
|Code=var x = new Boolean("true");
 if (x.constructor == Boolean)
     document.write("Object is a Boolelan.");

 // Output:
 // Object is a Boolean.
}}
}}
{{Remarks_Section
|Remarks=The '''constructor''' property contains a reference to the function that constructs instances of the Boolean object.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.6 15.6 Boolean Objects]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Boolean, Object
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155289(v=vs.94).aspx
|HTML5Rocks_link=
}}