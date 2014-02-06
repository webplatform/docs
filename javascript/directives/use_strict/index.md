{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Restricts the use of some potentially-harmful features of JavaScript (e.g. eval).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=use strict
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code causes a syntax error because in strict mode all variables must be declared with var.
|Code="use strict";
 function testFunction(){
    var testvar = 4;
     return testvar;
 }
 intvar = 5;
}}
}}
{{Remarks_Section
|Remarks=IE support: 10+
}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}