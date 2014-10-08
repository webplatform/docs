{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs to be moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the sticky flag ( '''y''' ) used with a regular expression. Default is '''false'''. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=rgExp.'''global'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the sticky property.
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
}}{{Single Example
|Language=JavaScript
|Description=Following is the resulting output.
|Code=global: true
 ignoreCase: false
 multiline: false
 Resulting String: The batter hit a ball with a bat and a fielder caught a ball with a glove.
}}
}}
{{Remarks_Section
|Remarks=The required rgExp reference is an instance of a '''Regular Expression''' object.

The <code>sticky</code> property returns '''true''' if the sticky flag is set for a regular expression, and returns '''false''' if it is not.

The global flag, when used, indicates that a search should find all occurrences of the pattern within the searched string, not just the first one. This is also known as global matching.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
}}
{{JS Topics
|JS Page Type=JS Property
|Applies to=RegExp
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}