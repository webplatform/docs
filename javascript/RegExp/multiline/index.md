{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value indicating the state of the multiline flag ( '''m''' ) used with a regular expression. Default is '''false'''. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= rgExp.'''multiline'''}}
}}
{{Remarks_Section
|Remarks=The required rgExp argument is an instance of the '''RegExp''' object

The '''multiline''' property returns '''true''' if the multiline flag is set for a regular expression, and returns '''false''' if it is not. The '''multiline''' property is '''true''' if the regular expression object was created with the '''m''' flag.

If '''multiline''' is '''false''' , "^" matches the position at the beginning of a string, and "$" matches the position at the end of a string. If '''multiline''' is '''true''' , "^" matches the position at the beginning of a string as well as the position following a "\n" or "\r", and "$" matches the position at the end of a string and the position preceding "\n" or "\r".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the behavior of the '''multiline''' property. If you pass "m" in to the function shown below, the word "while" is replaced with the word "and". This is because with the multiline flag is set and the word "while" occurs at the beginning of the line after a newline character. The multiline flag allows the search to be performed on multiline strings.

|Code= function RegExpMultilineDemo(flag){
    // The flag parameter is a string that contains
    // g, i, or m.  The flags can be combined.
 
    // Check flags for validity.
    if (flag.match(/[^gim]/))
       {
       return ("Flag specified is not valid");
       }
 
 
    // Create the string on which to perform the replacement.
    var ss = "The man hit the ball with the bat ";
    ss += "\nwhile the fielder caught the ball with the glove.";
 
    // Replace "while" with "and".
    var re = new RegExp("^while", flag);
    var r = ss.replace(re, "and");        
 
    // Output the multiline flag and the resulting string.
    var s = "";
    s += "Result for multiline = " + re.multiline.toString();
    s += ": " + r;
 
    return(s);
 
 }
 
 sa = RegExpMultilineDemo("m");
 sb = RegExpMultilineDemo("");
 document.write (sa + "&lt;br /&gt;" + sb);
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/global{{!}}global Property (Regular Expression)]]
* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/7f5z26w4(v=vs.94).aspx
|HTML5Rocks_link=
}}