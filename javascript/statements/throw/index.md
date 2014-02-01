{{Page_Title}}
{{Flags}}
{{Summary_Section|Generates an error condition that can be handled by a try...catch...finally statement.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= throw exception }}
}}
{{Remarks_Section
|Remarks=The required exception argument can be any expression.

The following example throws an error inside a try block, and it is caught in the catch block.

 try {
         throw new Error(200, "x equals zero");
 }
 catch (e) {
     document.write(e.message);
 }
 
 // Output: x equals zero.
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/try catch finally{{!}}try...catch...finally Statement]]
* [[javascript/Error{{!}}Error Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/85fscz6h(v=vs.94).aspx
|HTML5Rocks_link=
}}