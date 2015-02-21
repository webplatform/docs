{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the characters from the beginning of a searched string up to the position before the beginning of the last match. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''RegExp'''.'''leftContext'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''leftContext''' property:
|Code=// Create the regular expression pattern.
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";
 
    // Perform the search.
    var arr = re.exec(str);
 
    // Print the output.
    var s = "" 
    s += "$1: " + RegExp.$1 + "&lt;br /&gt;";
    s += "$2: " + RegExp.$2 + "&lt;br /&gt;";
    s += "$3: " + RegExp.$3 + "&lt;br /&gt;";
    s += "input: " + RegExp.input + "&lt;br /&gt;";
    s += "lastMatch: " + RegExp.lastMatch + "&lt;br /&gt;";
    s += "leftContext: " + RegExp.leftContext + "&lt;br /&gt;";
    s += "rightContext: " + RegExp.rightContext + "&lt;br /&gt;"; 
    s += "lastParen: " + RegExp.lastParen + "&lt;br /&gt;";
 
    document.write(s);
}}
}}
{{Remarks_Section
|Remarks=The object associated with this property is always the global '''RegExp''' object.

The initial value of the '''leftContext''' property is an empty string. The value of the '''leftContext''' property changes whenever a successful match is made.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/RegExp/1 9 Properties{{!}}$1...$9 Properties (RegExp)]]
* [[javascript/RegExp/index{{!}}index Property (RegExp)]]
* [[javascript/RegExp/input{{!}}input Property ($_) (RegExp)]]
* [[javascript/RegExp/lastIndex{{!}}lastIndex Property (RegExp)]]
* [[javascript/RegExp/lastMatch{{!}}lastMatch Property ($&#38;) (RegExp)]]
* [[javascript/RegExp/lastParen{{!}}lastParen Property ($+) (RegExp)]]
* [[javascript/RegExp/rightContext{{!}}rightContext Property ($') (RegExp)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0ch447h1(v=vs.94).aspx
|HTML5Rocks_link=
}}