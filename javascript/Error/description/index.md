{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns or sets the descriptive string associated with a specific error.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= object '''.description ''' [ '''= ''' stringExpression ]}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=Any instance of an Error object.}}{{JS_Syntax_Parameter
|Name=stringExpression
|Required=Optional
|Description=A string expression containing a description of the error.}}
}}
{{Remarks_Section
|Remarks=The '''description''' property contains the error message string associated with a specific error. Use the value contained in this property to alert a user to an error.

The '''description''' and '''message''' properties provide the same functionality; the '''description''' property provides backward compatibility; the '''message''' property complies with the ECMA standard.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''description''' property.

|Code= try
 {
 // Cause an error:
     x = y   
 }
 catch(e)
 {
 // Prints "[object Error]":
     document.write(e)
     document.write (" ");
 // Prints 5009:
     document.write((e.number &amp; 0xFFFF))  
     document.write (" ");
 // Prints "'y' is undefined":
     document.write(e.description);
     document.write (" ");
 // Prints "'y' is undefined":
     document.write(e.message)
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/number{{!}}number Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hs13sc3e(v=vs.94).aspx
|HTML5Rocks_link=
}}