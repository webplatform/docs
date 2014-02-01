{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the primitive value of the specified number.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= number.valueOf()}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=This method has no parameters.}}
}}
{{JS_Return_Value
|Description=Returns the number.}}
{{Remarks_Section
|Remarks=In the following example, the instantiated number object is the same as the return value of this method.

 var num = 1234;
 var s = num.valueOf();
 
 if (num === s)
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj159595(v=vs.94).aspx
|HTML5Rocks_link=
}}