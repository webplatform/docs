{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the characters from the position following the last match to the end of the searched string. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''RegExp'''.'''rightContext'''}}
}}
{{Remarks_Section
|Remarks=The object associated with this property is always the global '''RegExp''' object.

The initial value of the '''rightContext''' property is an empty string. The value of the '''rightContext''' property changes whenever a successful match is made.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''rightContext''' property:

|Code= // Create the regular expression pattern.
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
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/RegExp/1 9 Properties{{!}}$1...$9 Properties (RegExp)]]
* [[javascript/RegExp/index{{!}}index Property (RegExp)]]
* [[javascript/RegExp/input{{!}}input Property ($_) (RegExp)]]
* [[javascript/RegExp/lastIndex{{!}}lastIndex Property (RegExp)]]
* [[javascript/RegExp/lastMatch{{!}}lastMatch Property ($&#38;) (RegExp)]]
* [[javascript/RegExp/lastParen{{!}}lastParen Property ($+) (RegExp)]]
* [[javascript/RegExp/leftContext{{!}}leftContext Property ($`) (RegExp)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/b4sb5k1b(v=vs.94).aspx
|HTML5Rocks_link=
}}