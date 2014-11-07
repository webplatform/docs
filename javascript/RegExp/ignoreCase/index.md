{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Returns a Boolean value indicating the state of the ignoreCase flag ( '''i''' ) used with a regular expression. Default is '''false'''. Read-only.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=rgExp.'''ignoreCase'''
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
|Description=The following example illustrates the use of the '''ignoreCase''' property. If you pass "gi" in to the function shown below, all instances of the word "the" are replaced with the word "a", including the initial "The". This is because with the ignoreCase flag set, the search ignores any case sensitivity. So "T" is the same as "t" for the purposes of matching.

This function returns the Boolean values that indicate the state of the allowable regular expression flags, which are '''g''' , '''i''' , and '''m'''. The function also returns the string with all replacements made.
|Code=function RegExpPropDemo(flag){
     // The flag parameter is a string that contains
     // g, i, or m. The flags can be combined.
 
     // Check flags for validity.
     if (flag.match(/[^gim]/))
         {
         return ("Flag specified is not valid");
         }
 
     // Create the string on which to perform the replacement.
     var orig = "The batter hit the ball with the bat ";
     orig += "and the fielder caught the ball with the glove.";
 
     // Replace "the" with "a".
     var re = new RegExp("the", flag);
     var r = orig.replace(re, "a");        
 
     // Output the resulting string and the values of the flags.
     var s = "";
     s += "global: " + re.global.toString();
     s += "&lt;br /&gt;";
     s += "ignoreCase: " + re.ignoreCase.toString();
     s += "&lt;br /&gt;";
     s += "multiline: " + re.multiline.toString();
     s += "&lt;br /&gt;";
     s += "Resulting String: " + r;
     s += "&lt;br /&gt;";
     s += "&lt;br /&gt;";
     return (s);
 }
 
 document.write(RegExpPropDemo("gi"));
 document.write(RegExpPropDemo("g"));
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=Following is the resulting output.
|Code=global: true
 ignoreCase: true
 multiline: false
 Resulting String: a batter hit a ball with a bat and a fielder caught a ball with a glove.
 
 global: true
 ignoreCase: false
 multiline: false
 Resulting String: The batter hit a ball with a bat and a fielder caught a ball with a glove.
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required rgExp reference is an instance of the '''RegExp''' object.

The '''ignoreCase''' property returns '''true''' if the ignoreCase flag is set for a regular expression, and returns '''false''' if it is not.

The ignoreCase flag, when used, indicates that a search should ignore case sensitivity when matching the pattern within the searched string.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression/global{{!}}global Property (Regular Expression)]]
* [[javascript/regular expression/multiline{{!}}multiline Property (Regular Expression)]]
* [[javascript/regular expression/sticky{{!}}sticky Property (Regular Expression)]]
* [[javascript/regular expression/unicode{{!}}unicode Property (Regular Expression)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Property
|Applies to=RegExp
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/8kz93es5(v=vs.94).aspx
|HTML5Rocks_link=
}}