{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs to be moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the Unicode flag (<code>u</code>) used with a regular expression. Default is <code>false</code>. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=regex.'''unicode'''
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the Unicode property.
|Code=function RegExpPropDemo(flag){
    // The flag parameter is a string that contains
    // g, i, or m.  The flags can be combined.
 
    // Check flags for validity.
    if (flag.match(/[^gim]/))
       {
       return ("Flag specified is not valid");
       }
 
    // Create the string on which to perform the replacement.
    var ss = "The batter hit the ball with the bat ";
    ss += "and the fielder caught the ball with the glove.";
 
    //Replace "the" with "a".
    var re = new RegExp("the", flag);
    var r = ss.replace(re, "a");        
 
    // Output the resulting string and the flags.
    var s = "";
    s += "global: " + re.global.toString();
    s += "&lt;br /&gt;";
    s += "ignoreCase: " + re.ignoreCase.toString();
    s += "&lt;br /&gt;";
    s += "multiline: " + re.multiline.toString();
    s += "&lt;br /&gt;";
    s += "Resulting String: " + r;
 
    return (s);
 }
 
 document.write(RegExpPropDemo("g"));
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The <code>unicode</code> property returns <code>true</code> if the Unicode flag is set for a regular expression, and returns <code>false</code> if it is not.

The Unicode flag, when used, indicates …
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Topic_clusters=Javascript
|Manual_links=* [[javascript/regular expression/global{{!}}global Property (Regular Expression)]]
* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
* [[javascript/regular expression/sticky{{!}}sticky Property (Regular Expression)]]
|External_links=* [https://mathiasbynens.be/notes/es6-unicode-regex Unicode-aware regular expressions in ECMAScript 6]
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Property
|Applies to=RegExp
}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}