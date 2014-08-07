{{Page_Title|1...9 Properties}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Return the nine most-recently memorized portions found during pattern matching. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''RegExp'''.'''$''' n
}}
|Values={{JS Syntax Parameter
|Name='''RegExp'''
|Description=Always the global '''RegExp''' object.
}}{{JS Syntax Parameter
|Name=n
|Description=Any integer from 1 through 9.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example performs a regular expression search. It displays matches and submatches from the global '''RegExp''' object. The submatches are successful parenthesized matches that are contained in the '''...''' properties. The example also displays matches and submatches from the array that is returned by the '''exec''' method.
|Code=var newLine = "&lt;br /&gt;";
 
 var re = /(\w+)@(\w+)\.(\w+)/g
 var src = "Please send mail to george@contoso.com and someone@example.com. Thanks!"
 
 var result;
 var s = "";
 
 // Get the first match.
 result = re.exec(src);
 
 while (result != null) {
     // Show the entire match.
     s += newLine;
 
     // Show the match and submatches from the RegExp global object.
     s += "RegExp.lastMatch: " + RegExp.lastMatch + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
 
     // Show the match and submatches from the array that is returned
     // by the exec method.
     for (var index = 0; index &lt; result.length; index++) {
         s +=  index + ": ";
         s += result[index];
         s += newLine;
     }
 
     // Get the next match.
     result = re.exec(src);
 }
 document.write(s);
 
 // Output:
 //  RegExp.lastMatch: george@contoso.com
 //  RegExp.: george
 //  RegExp.: contoso
 //  RegExp.: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com
 
 //  RegExp.lastMatch: someone@example.com
 //  RegExp.: someone
 //  RegExp.: example
 //  RegExp.: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
}}
}}
{{Remarks_Section
|Remarks=The values of the '''$1...$9''' properties are modified whenever a successful parenthesized match is made. Any number of parenthesized substrings may be specified in a regular expression pattern, but only the nine most recent can be stored.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/24th3sah(v=vs.94).aspx
|HTML5Rocks_link=
}}