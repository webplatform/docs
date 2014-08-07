{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the character position where the next match begins in a searched string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''RegExp'''.'''lastIndex'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''lastIndex''' property. This function iterates a search string and prints out the '''index''' and '''lastIndex''' values for each word in the string.
|Code=function RegExpTest()
 {
    var ver = Number(ScriptEngineMajorVersion() + "." + ScriptEngineMinorVersion())
    if (ver &lt; 5.5)
    {
       document.write("You need a newer version of JavaScript for this to work");
       return;
    }
 
    var src = "The quick brown fox jumps over the lazy dog.";
 
    // Create regular expression pattern with a global flag.
    var re = /\w+/g;
 
    // Get the next word, starting at the position of lastindex.
    var arr;
    while ((arr = re.exec(src)) != null)
       {
       // New line:
       document.write ("&lt;br /&gt;");  
       document.write (arr.index + "-" + re.lastIndex + " ");
       document.write (arr);
       }
 }
}}
}}
{{Remarks_Section
|Remarks=The object associated with this property is always the global '''RegExp''' object.

The '''lastIndex''' property is zero-based, that is, the index of the first character is zero. Its initial value is -1. Its value is modified whenever a successful match is made.

The '''lastIndex''' property is modified by the '''exec''' and '''test''' methods of the '''RegExp''' object, and the '''match''' , '''replace''' , and '''split''' methods of the String object.

The following rules apply to values of '''lastIndex''' :

* If there is no match, '''lastIndex''' is set to -1.
* If '''lastIndex''' is greater than the length of the string, '''test''' and '''exec''' fail and '''lastIndex''' is set to -1.
* If '''lastIndex''' is equal to the length of the string, the regular expression matches if the pattern matches the empty string. Otherwise, the match fails and '''lastIndex''' is reset to -1.
* Otherwise, '''lastIndex''' is set to the next position following the most recent match.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9ec1ex6t(v=vs.94).aspx
|HTML5Rocks_link=
}}