{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a copy of the text of the regular expression pattern. Read-only. The rgExp argument is a '''Regular expression''' object. It can be a variable name or a literal.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= rgExp.'''source'''}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''source''' property:

|Code= function SourceDemo(re, s){
    var s1;
    // Test string for existence of regular expression.
    if (re.test(s))
       s1 = " contains ";
    else
       s1 = " does not contain ";
    // Get the text of the regular expression itself.
    return(s + s1 + re.source );
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression{{!}}Regular Expression Object]]
* [[javascript/regular expression{{!}}Regular Expression Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/fkd8dws9(v=vs.94).aspx
|HTML5Rocks_link=
}}