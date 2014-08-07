{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the value of a string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=string.valueOf()
}}
|Values={{JS Syntax Parameter
|Description=This method has no parameters.
}}
}}
{{JS_Return_Value
|Description=Returns the string value.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155295(v=vs.94).aspx
|HTML5Rocks_link=
}}