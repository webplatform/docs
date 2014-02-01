{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value that indicates whether or not a pattern exists in a searched string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= rgExp.'''test(''' str ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=rgExp
|Required=Required
|Description=An instance of a '''Regular Expression''' object containing the regular expression pattern and applicable flags.}}{{JS_Syntax_Parameter
|Name=str
|Required=Required
|Description=The string on which to perform the search.}}
}}
{{Remarks_Section
|Remarks=The '''test''' method checks to see if a pattern exists within a string and returns '''true''' if so, and '''false''' otherwise.

The properties of the global '''RegExp''' object are not modified by the '''test''' method.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''test''' method. To use this example, pass the function a regular expression pattern and a string. The function will test for the occurrence of the regular expression pattern in the string and return a string indicating the results of that search:

|Code= function TestDemo(re, teststring)
 {
    // Test string for existence of regular expression.
    var found = re.test(teststring)
 
    // Format the output.
    var s = "";
    s += "'" + teststring + "'"
 
    if (found)
       s += " contains ";
    else
       s += " does not contain ";
       
    s += "'" + re.source + "'"
    return(s);
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/RegExp{{!}}RegExp Object]]
* [[javascript/regular expression{{!}}Regular Expression Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/a55e5s6b(v=vs.94).aspx
|HTML5Rocks_link=
}}