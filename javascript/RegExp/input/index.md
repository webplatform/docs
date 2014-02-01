{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the string against which a regular expression search was performed. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''RegExp'''.'''input'''}}
}}
{{Remarks_Section
|Remarks=The object associated with this property is always the global '''RegExp''' object.

The value of '''input''' property is modified any time the searched string is changed.

The following example illustrates the use of the '''input''' property:

 function inputDemo(){
    var s;
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";
    var arr = re.exec(str);
    s = "The string used for the match was " + RegExp.input ; 
    return(s);
 }
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dsa56hkc(v=vs.94).aspx
|HTML5Rocks_link=
}}