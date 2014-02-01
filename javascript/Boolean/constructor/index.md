{{Page_Title}}
{{Flags}}
{{Summary_Section|Specifies the function that creates a Boolean.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= boolean.constructor([[ value ])}}
|Values={{JS_Syntax_Parameter
|Name=boolean
|Required=
|Description=The name of the Boolean.}}{{JS_Syntax_Parameter
|Name=value
|Required=Optional
|Description=Specifies the value of the Boolean. This can be the numbers 1 or 0, or the strings "true" or "false".}}
}}
{{Remarks_Section
|Remarks=The '''constructor''' property contains a reference to the function that constructs instances of the Boolean object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the constructor property.

|Code= var x = new Boolean("true");
 
 if (x.constructor == Boolean)
     document.write("Object is a Boolelan.");
 
 // Output:
 // Object is a Boolean.
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155289(v=vs.94).aspx
|HTML5Rocks_link=
}}