{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the string against which a regular expression search was performed. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''RegExp'''.'''input'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The object associated with this property is always the global '''RegExp''' object.

The value of '''input''' property is modified any time the searched string is changed.

The following example illustrates the use of the '''input''' property:
|Code=function inputDemo() {
    var s;
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";
    var arr = re.exec(str);
    s = "The string used for the match was " + RegExp.input ; 
    return(s);
}
}}
}}
{{Remarks_Section}}
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dsa56hkc(v=vs.94).aspx
|HTML5Rocks_link=
}}