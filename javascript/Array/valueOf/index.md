{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the primitive value of the specified object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= array.valueOf()}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=This method has no parameters.}}
}}
{{JS_Return_Value
|Description=Returns the array instance.}}
{{Remarks_Section
|Remarks=In the following example, the instantiated array object is the same as the return value of this method.

 var arr = [1, 2, 3, 4];
 var s = arr.valueOf();
 
 if (arr === s)
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155290(v=vs.94).aspx
|HTML5Rocks_link=
}}