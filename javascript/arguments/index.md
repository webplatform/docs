{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|An object representing the arguments to the currently executing function, and the functions that called it.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=[ function '''.''' ] '''arguments[''' n ''']'''
}}
|Values={{JS Syntax Parameter
|Name=function
|Required=Optional
|Description=The name of the currently executing Function object.
}}{{JS Syntax Parameter
|Name=n
|Required=Required
|Description=The zero-based index to argument values passed to the Function object.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''arguments''' object.
|Code=function ArgTest(a, b)
 {
    var s = "";
 
    s += "Expected Arguments: " + ArgTest.length;
    s += "&lt;br /&gt;";
    s += "Passed Arguments: " + arguments.length;
    s += "&lt;br /&gt;";
 
    s += "The individual arguments are: "
    for (n = 0; n &lt; arguments.length; n++)
    {
       s += ArgTest.arguments[n];
       s += " ";
    }
 
    document.write(s);
 }
 
 ArgTest(1, 2, "hello", new Date())
 
 // Output:
 // Expected Arguments: 2
 // Passed Arguments: 4
 // The individual arguments are: 1 2 hello Tues Jan 8 08:27:09 PST 20xx
}}
}}
{{Remarks_Section
|Remarks=You cannot explicitly create an '''arguments''' object. The '''arguments''' object only becomes available when a function begins execution. The '''arguments''' object of the function is not an array, but the individual arguments are accessed the same way array elements are accessed. The index n is actually a reference to one of the '''0''' n properties of the '''arguments''' object.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/arguments/0 n Properties{{!}}0...n Properties (arguments)]]
* [[javascript/arguments/callee{{!}}callee Property (arguments)]]
* [[javascript/arguments/length{{!}}length Property (arguments)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/87dw3w1k(v=vs.94).aspx
|HTML5Rocks_link=
}}