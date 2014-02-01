{{Page_Title}}
{{Flags}}
{{Summary_Section|Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= rgExp.'''exec(''' str ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=rgExp
|Required=Required
|Description=An instance of a '''Regular Expression''' object containing the regular expression pattern and applicable flags.}}{{JS_Syntax_Parameter
|Name=str
|Required=Required
|Description=The String object or string literal on which to perform the search.}}
}}
{{Remarks_Section
|Remarks=If the '''exec''' method does not find a match, it returns null. If it finds a match, '''exec''' returns an array, and the properties of the global '''RegExp''' object are updated to reflect the results of the match. Element zero of the array contains the entire match, while elements 1 - n contain any submatches that have occurred within the match. This behavior is identical to the behavior of the '''match''' method without the global flag ( '''g''' ) set.

If the global flag is set for a regular expression, '''exec''' searches the string beginning at the position indicated by the value of '''lastIndex'''. If the global flag is not set, '''exec''' ignores the value of '''lastIndex''' and searches from the beginning of the string.

The array returned by the '''exec''' method has three properties, '''input''' , '''index''' and '''lastIndex.''' The '''input''' property contains the entire searched string. The '''index''' property contains the position of the matched substring within the complete searched string. The '''lastIndex''' property contains the position following the last character in the match.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''exec''' method:

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
       document.write (arr[0]);
       }
 }
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String/match{{!}}match Method (String)]]
* [[javascript/RegExp{{!}}RegExp Object]]
* [[javascript/String/search{{!}}search Method (String)]]
* [[javascript/regular expression/test{{!}}test Method (Regular Expression)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/z908hy33(v=vs.94).aspx
|HTML5Rocks_link=
}}