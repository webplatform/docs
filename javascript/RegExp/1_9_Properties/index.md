{{Page_Title}}
{{Flags}}
{{Summary_Section|Return the nine most-recently memorized portions found during pattern matching. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''RegExp'''.'''$''' n }}
|Values={{JS_Syntax_Parameter
|Name='''RegExp'''
|Required=
|Description=Always the global '''RegExp''' object.}}{{JS_Syntax_Parameter
|Name=n
|Required=
|Description=Any integer from 1 through 9.}}
}}
{{Remarks_Section
|Remarks=The values of the '''$1...$9''' properties are modified whenever a successful parenthesized match is made. Any number of parenthesized substrings may be specified in a regular expression pattern, but only the nine most recent can be stored.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example performs a regular expression search. It displays matches and submatches from the global '''RegExp''' object. The submatches are successful parenthesized matches that are contained in the '''$1...$9''' properties. The example also displays matches and submatches from the array that is returned by the '''exec''' method.

|Code= var newLine = "&lt;br /&gt;";
 
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
     s += "RegExp.$1: " + RegExp.$1 + newLine;
     s += "RegExp.$2: " + RegExp.$2 + newLine;
     s += "RegExp.$3: " + RegExp.$3 + newLine;
 
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
 //  RegExp.$1: george
 //  RegExp.$2: contoso
 //  RegExp.$3: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com
 
 //  RegExp.lastMatch: someone@example.com
 //  RegExp.$1: someone
 //  RegExp.$2: example
 //  RegExp.$3: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/24th3sah(v=vs.94).aspx
|HTML5Rocks_link=
}}