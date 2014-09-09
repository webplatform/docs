{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|Content=Incomplete, Compatibility Incomplete
}}
{{Summary_Section|Restricts the use of some potentially-harmful features of JavaScript (e.g., '''eval''', '''with''') and throws syntax errors for certain sloppy code.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format="use strict";
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code causes a syntax error because in strict mode all variables must be declared with <code>var</code>.
|Code=// Be careful - all code used in the page/context must be strict mode conformant.
"use strict";
function testFunction(){
   var testvar = 4;
    return testvar;
}
intvar = testFunction();
}}{{Single Example
|Language=JavaScript
|Description=The following code causes a syntax error because in strict mode all variables must be declared with <code>var</code>. Even though the strict mode directive (<code>use strict;</code>) is only added to the function, the whole code breaks because that function does not adhere to the strict mode rules.
|Code=function testFunction(){
   // Restricts strict mode to this function only.
   "use strict";
   // This will throw.
   testvar = 4;
   return testvar;
}
var hello = true;
}}{{Single Example
|Language=JavaScript
|Description=The following code _does not_ cause a syntax error, even though the variable '''intvar''' variable is not declared with <code>var</code>, because the strict mode is scoped to the function only, while the non conformant code is found in a different scope (the global scope).
|Code=function testFunction(){
   // Restricts strict mode to this function only.
   "use strict";
   var testvar = 4;
   return testvar;
}

// This would have caused a syntax error to be thrown if there had been
// a "use strict"; directive at the top of the script (above the testFunction
// function). Since the directive is scoped to the function and not to the
// global scope (in which this code operates), this code runs normally.
intvar = 1;
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
When the expression <code>"use strict";</code> is placed at the start of a script or a function body, the code contained in it is parsed under stricter rules than what the default JavaScript language allows.
These rules include:
* Variables must be explicitly declared (<code>var</code>).
* Statements must end with a semicolon (<code>;</code>).
* Assigning values to a read-only property fails (<code>Node.DOCUMENT_FRAGMENT_NODE = 9;</code>).
*'''with''' statements are completely disallowed.
{{TODO|Add the complete set of strict mode rules.}}
{{See_Also_Section
|Manual_sections=
{{{!}} class="wikitable"
{{!}}-
!Browser
!Supported versions
{{!}}-
{{!}}Internet Explorer
{{!}}10 and higher
{{!}}-
{{!}}Chrome
{{!}}13 and higher
{{!}}-
{{!}}Firefox
{{!}}4 and higher
{{!}}-
{{!}}Opera
{{!}}11.6 and higher
{{!}}-
{{!}}Safari
{{!}}6 and higher
{{!}}-
{{!}}Mobile Safari
{{!}}5.1 and higher
{{!}}-
{{!}}Android browser
{{!}}3 and higher
{{!}}-
{{!}}Opera Mobile
{{!}}11.5 and higher
{{!}}-
{{!}}Internet Explorer Mobile
{{!}}10 and higher
{{!}}-
{{!}}Firefox for Android
{{!}}4 and higher
{{!}}-
{{!}}Chrome for Android
{{!}}18 and higher
{{!}}}
*Safari 5 - 5.1 partially supports this feature.
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}