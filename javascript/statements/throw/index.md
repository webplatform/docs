{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Generates an error condition that can be handled by a try...catch...finally statement.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=throw exception
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example throws an error inside a try block, and it is caught in the catch block.
|Code=try {
         throw new Error(200, "x equals zero");
 }
 catch (e) {
     document.write(e.message);
 }
 
 // Output: x equals zero.
}}
}}
{{Remarks_Section
|Remarks=The required exception argument can be any expression.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/try catch finally{{!}}try...catch...finally Statement]]
* [[javascript/Error{{!}}Error Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/85fscz6h(v=vs.94).aspx
|HTML5Rocks_link=
}}