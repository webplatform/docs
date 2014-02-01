{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the natural logarithm (base e ) of a number.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Math.log( number ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=number
|Required=
|Description=A number.}}
}}
{{JS_Return_Value
|Description=If number is positive, this function returns the natural logarithm of the number. If number is negative, this function returns NaN. If number is 0, this function returns -Infinity.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use this function.

|Code= var numArr = [ 45.3, 69.0, 557.04, 0.222 ];
 
 for (i in numArr) {
     document.write(Math.log(numArr[i]));
     document.write("&lt;br/&gt;");
 }
 
 // Output: 
 // 3.8133070324889884
 // 4.23410650459726
 // 6.322637050634291
 // -1.5050778971098575
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/sqrt{{!}}Math.sqrt Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}