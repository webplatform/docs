{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the character position where the first successful match begins in a searched string. Read-only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''RegExp'''.'''index''' }}
}}
{{Remarks_Section
|Remarks=The object associated with this property is always the global '''RegExp''' object.

The '''index''' property is zero-based. The initial value of the '''index''' property is -1. Its value changes whenever a successful match is made.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''index''' property. This function iterates a search string and prints out the '''index''' and '''lastIndex''' values for each word in the string.

|Code= function RegExpTest()
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
       document.write (arr.index + "-" + arr.lastIndex + " ");
       document.write (arr);
       }
 }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0xsw26xd(v=vs.94).aspx
|HTML5Rocks_link=
}}