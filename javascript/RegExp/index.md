{{Page_Title}}
{{Flags}}
{{Summary_Section|An intrinsic global object that stores information about the results of regular expression pattern matches.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''RegExp'''.property }}
}}
{{Remarks_Section
|Remarks=The required property argument can be any one of the '''RegExp''' object properties.

The '''RegExp''' object cannot be created directly, but is always available for use. Until a successful regular expression search has been completed, the initial values of the various properties of the '''RegExp''' object are as follows:

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

The global '''RegExp''' object should not be confused with the '''Regular Expression''' object. Even though they sound like the same thing, they are separate and distinct. The properties of the global '''RegExp''' object contain continually updated information about each match as it occurs, while the properties of the '''Regular Expression''' object contain only information about the matches that occur with that instance of the '''Regular Expression'''.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example performs a regular expression search. It displays matches and submatches from the global '''RegExp''' object, and from the array that is returned by the '''exec''' method.

|Code= var newLine = "&lt;br /&gt;";
 
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
     s += "RegExp.$1: " + RegExp.$1 + newLine;
     s += "RegExp.$2: " + RegExp.$2 + newLine;
     s += "RegExp.$3: " + RegExp.$3 + newLine;
 
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
 //  RegExp.$1: george
 //  RegExp.$2: contoso
 //  RegExp.$3: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com
 
 //  RegExp.lastMatch: someone@example.com
 //  RegExp.$1: someone
 //  RegExp.$2: example
 //  RegExp.$3: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
}}}}
==Properties==
[[javascript/RegExp/1 9 Properties|rightContext Property]]
==Methods==
The '''RegExp''' object has no methods.
{{See_Also_Section
|Manual_links=* [[javascript/regular expression{{!}}Regular Expression Object]]
* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9dthzd08(v=vs.94).aspx
|HTML5Rocks_link=
}}