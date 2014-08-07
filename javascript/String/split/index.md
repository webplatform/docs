{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Split a string into substrings using the specified separator and return the substrings as an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=stringObj.split([separator[, limit ]])
}}
|Values={{JS Syntax Parameter
|Name=stringObj
|Required=Required
|Description=The String object or string literal to be split. This object is not modified by the '''split''' method.
}}{{JS Syntax Parameter
|Name=separator
|Required=Optional
|Description=A string or a '''Regular Expression''' object that identifies character or characters to use in separating the string. If omitted, a single-element array containing the entire string is returned.
}}{{JS Syntax Parameter
|Name=limit
|Required=Optional
|Description=A value used to limit the number of elements returned in the array.
}}
}}
{{JS_Return_Value
|Description=The result of the '''split''' method is an array of strings split at each point where separator occurs in stringObj. The separator is not returned as part of any array element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''split''' method.
|Code=var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.split(" ");
 for (i in ss) {
     document.write(ss[i];
     document.write("&lt;br/&gt;");
 }
 
 // Output: 
 // The
 // quick
 // brown
 // fox
 // jumps
 // over
 // the
 // lazy
 // dog.
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/concat{{!}}concat Method (String)]]
* [[javascript/RegExp{{!}}RegExp Object]]
* [[javascript/regular expression{{!}}Regular Expression Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t5az126b(v=vs.94).aspx
|HTML5Rocks_link=
}}