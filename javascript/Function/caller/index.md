{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the function that invoked the current function.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= functionName.caller}}
}}
{{Remarks_Section
|Remarks=The functionName object is the name of any executing function.

The '''caller''' property is defined for a function only while that function is executing. If the function is called from the top level of a JavaScript program, '''caller''' contains null.

If the '''caller''' property is used in a string context, the result is the same as functionName.'''toString''' , that is, the decompiled text of the function is displayed.

The following example illustrates the use of the '''caller''' property:

 function CallLevel(){
    if ( CallLevel.caller == null)
       return("CallLevel was called from the top level.");
    else
       return("CallLevel was called by another function.");
 }
 
 document.write(CallLevel());
 
 // Output: CallLevel was called from the top level.
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7t96kt3h(v=vs.94).aspx
|HTML5Rocks_link=
}}