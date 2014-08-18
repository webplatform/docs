{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns or sets the descriptive string associated with a specific error.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=object '''.description ''' [ '''= ''' stringExpression ]
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=Any instance of an Error object.
}}{{JS Syntax Parameter
|Name=stringExpression
|Required=Optional
|Description=A string expression containing a description of the error.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''description''' property.
|Code=try
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
}}
}}
{{Remarks_Section
|Remarks=The '''description''' property contains the error message string associated with a specific error. Use the value contained in this property to alert a user to an error.

The '''description''' and '''message''' properties provide the same functionality; the '''description''' property provides backward compatibility; the '''message''' property complies with the ECMA standard.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Error/number{{!}}number Property (Error)]]
* [[javascript/Error/message{{!}}message Property (Error)]]
* [[javascript/Error/name{{!}}name Property (Error)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hs13sc3e(v=vs.94).aspx
|HTML5Rocks_link=
}}