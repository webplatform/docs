{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the current date and time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Date.now()}}
}}
{{JS_Return_Value
|Description=The number of milliseconds between midnight, January 1, 1970, and the current date and time.}}
{{Remarks_Section
|Remarks=The [[javascript/Date/getTime{{!}}getTime method]] returns the number of milliseconds between January 1, 1970, and a specified date.

For information about how to calculate elapsed time and compare dates, see Date and Time Calculations (Windows Scripting - JScript).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''now''' method.

|Code= var start = Date.now();
 var response = prompt("What is your name?", "");
 var end = Date.now();
 var elapsed = (end - start) / 1000;
 document.write("You took " + elapsed + " seconds" + " to type: " + response);
 
 // Output:
 // You took &lt;seconds&gt; seconds to type: &lt;name&gt;
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getTime{{!}}getTime Method (Date)]]
* [[javascript/Date{{!}}Date Object]]
* [[javascript/methods{{!}}JavaScript Methods]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679974(v=vs.94).aspx
|HTML5Rocks_link=
}}