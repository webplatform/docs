{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a Boolean value indicating the state of the global flag ( '''g''' ) used with a regular expression. Default is '''false'''. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= rgExp.'''global'''}}
}}
{{Remarks_Section
|Remarks=The required rgExp reference is an instance of a '''Regular Expression''' object.

The global property returns '''true''' if the global flag is set for a regular expression, and returns '''false''' if it is not.

The global flag, when used, indicates that a search should find all occurrences of the pattern within the searched string, not just the first one. This is also known as global matching.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the global property. If you pass '''g''' in to the function shown below, all instances of the word "the" are replaced with the word "a". Note that the "The" at the beginning of the string is not replaced because the '''i''' (ignore case) flag is not passed to the function.

This function displays the condition of the properties associated with the allowable regular expression flags, which are '''g''' , '''i''' , and '''m'''. The function also displays the string with all replacements made.

|Code= function RegExpPropDemo(flag){
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
}}{{Single_Example
|Language=JavaScript
|Description=Following is the resulting output.

|Code= global: true
 ignoreCase: false
 multiline: false
 Resulting String: The batter hit a ball with a bat and a fielder caught a ball with a glove.
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/ignoreCase{{!}}ignoreCase Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/2789hxff(v=vs.94).aspx
|HTML5Rocks_link=
}}