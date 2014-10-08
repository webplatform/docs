{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|An intrinsic global object that stores information about the results of regular expression pattern matches.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''RegExp'''.property
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example performs a regular expression search. It displays matches and submatches from the global '''RegExp''' object, and from the array that is returned by the '''exec''' method.
|Code=var newLine = "&lt;br /&gt;";
 
 var re = /(\w+)@(\w+)\.(\w+)/g
 var src = "Please send mail to george@contoso.com and someone@example.com. Thanks!"
 
 var result;
 var s = "";
 
 // Get the first match.
 result = re.exec(src);
 
 while (result != null) {
     // Show the entire match.
     s += newLine;
 
     // Show the match and submatches from the RegExp global object.
     s += "RegExp.lastMatch: " + RegExp.lastMatch + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
 
     // Show the match and submatches from the array that is returned
     // by the exec method.
     for (var index = 0; index &lt; result.length; index++) {
         s +=  index + ": ";
         s += result[index];
         s += newLine;
     }
 
     // Get the next match.
     result = re.exec(src);
 }
 document.write(s);
 
 // Output:
 //  RegExp.lastMatch: george@contoso.com
 //  RegExp.: george
 //  RegExp.: contoso
 //  RegExp.: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com
 
 //  RegExp.lastMatch: someone@example.com
 //  RegExp.: someone
 //  RegExp.: example
 //  RegExp.: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
}}
}}
{{Remarks_Section
|Remarks=The required property argument can be any one of the <code>RegExp</code> object properties.

The <code>RegExp</code> object cannot be created directly, but is always available for use. Until a successful regular expression search has been completed, the initial values of the various properties of the <code>RegExp</code> object are as follows:

{{{!}} class='wikitable'
{{!}}-
! Property
! Shorthand
! Initial Value
{{!}}-
{{!}} index
{{!}} -1
{{!}}-
{{!}} input
{{!}} $_
{{!}} Empty string.
{{!}}-
{{!}} lastIndex
{{!}} -1
{{!}}-
{{!}} lastMatch
{{!}} $&amp;
{{!}} Empty string.
{{!}}-
{{!}} lastParen
{{!}} $+
{{!}} Empty string.
{{!}}-
{{!}} leftContext
{{!}} $`
{{!}} Empty string.
{{!}}-
{{!}} rightContext
{{!}} $'
{{!}} Empty string.
{{!}}-
{{!}} $1 - $9
{{!}} $1 - $9
{{!}} Empty string.
{{!}}} 
Its properties have undefined as their value until a successful regular expression search has been completed.

The global <code>RegExp</code> object should not be confused with the '''Regular Expression''' object. Even though they sound like the same thing, they are separate and distinct. The properties of the global <code>RegExp</code> object contain continually updated information about each match as it occurs, while the properties of the '''Regular Expression''' object contain only information about the matches that occur with that instance of the '''Regular Expression'''.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/regular expression{{!}}Regular Expression Object]]
* [[javascript/String{{!}}String Object]]
}}
{{JS Topics
|JS Page Type=JS Object
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9dthzd08(v=vs.94).aspx
|HTML5Rocks_link=
}}