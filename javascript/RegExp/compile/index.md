{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs to be moved under javascript/RegExp
|Checked_Out=No
}}
{{Summary_Section|Compiles a regular expression into an internal format for faster execution.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=rgExp.'''compile(''' pattern , [ flags ] ''')'''
}}
|Values={{JS Syntax Parameter
|Name=rgExp
|Required=Required
|Description=An instance of a '''Regular Expression''' object. Can be a variable name or a literal.
}}{{JS Syntax Parameter
|Name=pattern
|Required=Required
|Description=A string expression containing a regular expression pattern to be compiled
}}{{JS Syntax Parameter
|Name=flags
|Required=Optional
|Description=Available flags, which may be combined, are: <code>g</code> (global search for all occurrences of the pattern), <code>i</code> (ignore case), <code>m</code> (multiline search), <code>u</code> (Unicode), <code>y</code> (sticky matching), 
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''compile''' method:
|Code=function CompileDemo(){
    var rs;
    var s = "AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPp"
    // Create regular expression for uppercase only.
    var r = new RegExp("[A-Z]", "g");
    var a1 = s.match(r)              // Find matches.
    // Compile the regular expression for lowercase only.r.compile( "[a-z]" , "g" ) ;
 // Find matches.
    var a2 = s.match(r)              
    return(a1 + "\n" + a2);
 }
}}
}}
{{Remarks_Section
|Remarks=The '''compile''' method converts pattern into an internal format for faster execution. This allows for more efficient use of regular expressions in loops, for example. A compiled regular expression speeds things up when reusing the same expression repeatedly. No advantage is gained, however, if the regular expression changes.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=RegExp
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/x9cswe0z(v=vs.94).aspx
|HTML5Rocks_link=
}}