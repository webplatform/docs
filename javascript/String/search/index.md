{{Page_Title}}
{{Flags}}
{{Summary_Section|Finds the first substring match in a regular expression search.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringObj.search( rgExp ) }}
|Values={{JS_Syntax_Parameter
|Name=stringObj
|Required=Required
|Description=The String object or string literal on which to perform the search.}}{{JS_Syntax_Parameter
|Name=rgExp
|Required=Required
|Description=An instance of a '''Regular Expression''' object containing the regular expression pattern and applicable flags.}}
}}
{{JS_Return_Value
|Description=If a match is found, the '''search''' method returns an integer value that indicates the offset from the beginning of the string where the first match occurred. If no match is found, it returns -1.}}
{{Remarks_Section
|Remarks=You can also set the i flag that causes the search to be case-insensitive.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''search''' method.

|Code= var src = "is but a Dream within a dream";
 var re = /dream/;
 var pos = src.search(re);
 document.write(pos);
 document.write("&lt;br/&gt;");
 
 re = /dream/i;
 pos = src.search(re);
 document.write(pos);
 
 // Output: 
 // 24 
 // 9
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/exec{{!}}exec Method (Regular Expression)]]
* [[javascript/String/match{{!}}match Method (String)]]
* [[javascript/regular expression{{!}}Regular Expression Object]]
* [[javascript/String/replace{{!}}replace Method (String)]]
* [[javascript/regular expression/test{{!}}test Method (Regular Expression)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/tbc7a78k(v=vs.94).aspx
|HTML5Rocks_link=
}}