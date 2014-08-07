{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Matches a string with a regular expression, and returns an array containing the results of that search.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=stringObj.match( rgExp )
}}
|Values={{JS Syntax Parameter
|Name=stringObj
|Required=Required
|Description=The String object or string literal on which to perform the search.
}}{{JS Syntax Parameter
|Name=rgExp
|Required=Required
|Description=A regular expression object that contains the regular expression pattern and applicable flags. This can also be a variable name or string literal containing the regular expression pattern and flags.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the match method.
|Code=var src = "azcafAJAC";
 
 var re = /[a-c]/;
 
 var result = src.match(re);
 
 // The entire match is in array element 0.
 document.write(result[0] + "&lt;br/&gt;");
 
 // Now try the same match with the global flag.
 var reg = /[a-c]/g;
 result = src.match(reg);
 
 
 // The matches are in elements 0 through n.
 for (var index = 0; index &lt; result.length; index++)
 {
     document.write ("submatch " + index + ": " +  result[index]);
     document.write("&lt;br /&gt;");
 }
}}
}}
{{Remarks_Section
|Remarks=If the '''match''' method does not find a match, it returns null. If it finds a match, '''match''' returns an array, and the properties of the global '''RegExp''' object are updated to reflect the results of the match.

The array returned by the '''match''' method has three properties, '''input''' , '''index''' and '''lastIndex'''. The input property contains the entire searched string. The index property contains the position of the matched substring within the complete searched string. The '''lastIndex''' property contains the position following the last character in the last match.

If the global flag ( '''g''' ) is not set, Element zero of the array contains the entire match, while elements 1 through n contain any submatches. This behavior is the same as the behavior of the [[javascript/regular expression/exec{{!}}exec Method (Regular Expression)]] when the global flag is not set. If the global flag is set, elements 0 through n contain all matches that occurred.

If the flag '''i''' is set, the search is not case-sensitive.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/exec{{!}}exec Method (Regular Expression)]]
* [[javascript/RegExp{{!}}RegExp Object]]
* [[javascript/regular expression{{!}}Regular Expression Object]]
* [[javascript/String/replace{{!}}replace Method (String)]]
* [[javascript/String/search{{!}}search Method (String)]]
* [[javascript/regular expression/test{{!}}test Method (Regular Expression)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7df7sf4x(v=vs.94).aspx
|HTML5Rocks_link=
}}