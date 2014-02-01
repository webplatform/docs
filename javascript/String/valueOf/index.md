{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= string.valueOf()}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=This method has no parameters.}}
}}
{{JS_Return_Value
|Description=Returns the string value.}}
{{Remarks_Section
|Remarks=In the following example, the string object is the same as the return value.

 var str = "every good boy does fine";
 var strStr = str.valueOf();
 
 if (str === strStr)
 document.write("same");
 else
 document.write("different");
 
 // Output:
 // same
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155295(v=vs.94).aspx
|HTML5Rocks_link=
}}