{{Page_Title}}
{{Flags}}
{{Summary_Section|Restricts the use of some features in JavaScript. Supported in Internet Explorer 10 and Windows Store apps only.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= use strict}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code causes a syntax error because in strict mode all variables must be declared with var.

|Code= "use strict";
 function testFunction(){
    var testvar = 4;
     return testvar;
 }
 intvar = 5;
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}