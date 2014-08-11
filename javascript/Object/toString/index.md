{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a string representation of an object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=objectname.toString([ radix ])
}}
|Values={{JS Syntax Parameter
|Name=objectname
|Required=Required
|Description=An object for which a string representation is sought.
}}{{JS Syntax Parameter
|Name=radix
|Required=Optional
|Description=Specifies a radix for converting numeric values to strings. This value is only used for numbers.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with a radix argument. The return value of function shown below is a Radix conversion table.
|Code=function CreateRadixTable (){
    var s = "";
 
    // Create table heading.
    s += "Hex  Dec  Bin \n";
 
    for (x = 0; x &lt; 16; x++)
    {
       s += "   ";
 
       // Convert to hexidecimal.
       s += x.toString(16);
       s += "     ";
       if (x &lt; 10) s += "  ";
 
       // Convert to decimal.
       s += x.toString(10);
       s += "     ";
 
       // Convert to binary.
       s += x.toString(2);
       s += "\n";
    }
 
    return(s);
 }
}}
}}
{{Remarks_Section
|Remarks=The '''toString''' method is a member of all built-in JavaScript objects. How it behaves depends on the object type:

{{{!}} class='wikitable'
{{!}}-
! Object
! Behavior
{{!}}-
{{!}} Array
{{!}} Elements of an '''Array''' are converted to strings. The resulting strings are concatenated, separated by commas.
{{!}}-
{{!}} Boolean
{{!}} If the Boolean value is '''true''' , returns " <code>true</code> ". Otherwise, returns " <code>false</code> ".
{{!}}-
{{!}} Date
{{!}} Returns the textual representation of the date.
{{!}}-
{{!}} Error
{{!}} Returns a string containing the associated error message.
{{!}}-
{{!}} Function
{{!}} Returns a string of the following form, where functionname is the name of the function whose '''toString''' method was called:Copy Code function functionname( ) { [native code] }
{{!}}-
{{!}} Number
{{!}} Returns the textual representation of the number.
{{!}}-
{{!}} String
{{!}} Returns the value of the String object.
{{!}}-
{{!}} Default
{{!}} Returns <code>"[object objectname]"</code> , where <code>objectname</code> is the name of the object type.
{{!}}}
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/k6xhc6yc(v=vs.94).aspx
|HTML5Rocks_link=
}}