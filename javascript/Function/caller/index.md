{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the function that invoked the current function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=functionName.caller
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''caller''' property:
|Code= function CallLevel(){
    if ( CallLevel.caller == null)
       return("CallLevel was called from the top level.");
    else
       return("CallLevel was called by another function.");
 }
 
 document.write(CallLevel());
 
 // Output: CallLevel was called from the top level.
}}
}}
{{Remarks_Section
|Remarks=The functionName object is the name of any executing function.

The '''caller''' property is defined for a function only while that function is executing. If the function is called from the top level of a JavaScript program, '''caller''' contains null.

If the '''caller''' property is used in a string context, the result is the same as functionName.'''toString''' , that is, the decompiled text of the function is displayed.


}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7t96kt3h(v=vs.94).aspx
|HTML5Rocks_link=
}}