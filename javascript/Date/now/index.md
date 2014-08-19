{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the current date and time.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Date.now()
}}
|Values=
}}
{{JS_Return_Value
|Description=The number of milliseconds between midnight, January 1, 1970, and the current date and time.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''now''' method.
|Code=var start = Date.now();
 var response = prompt("What is your name?", "");
 var end = Date.now();
 var elapsed = (end - start) / 1000;
 document.write("You took " + elapsed + " seconds" + " to type: " + response);
 
 // Output:
 // You took &lt;seconds&gt; seconds to type: &lt;name&gt;
}}
}}
{{Remarks_Section
|Remarks=The [[javascript/Date/getTime{{!}}getTime method]] returns the number of milliseconds between January 1, 1970, and a specified date.

For information about how to calculate elapsed time and compare dates, see Date and Time Calculations (Windows Scripting - JScript).
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getTime{{!}}getTime Method (Date)]]
* [[javascript/Date{{!}}Date Object]]
* [[javascript/methods{{!}}JavaScript Methods]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679974(v=vs.94).aspx
|HTML5Rocks_link=
}}