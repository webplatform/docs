{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a string representation of an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= array.toString()}}
|Values={{JS_Syntax_Parameter
|Name=array
|Required=Required
|Description=The array to represent as a string.}}
}}
{{JS_Return_Value
|Description=The string representation of the array.}}
{{Remarks_Section
|Remarks=The elements of an '''Array''' are converted to strings. The resulting strings are concatenated and separated by commas.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with an array.

|Code= var arr = [1, 2, 3, 4];
 var s = arr.toString();
 document.write(s);
 
 // Output: 1,2,3,4
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155287(v=vs.94).aspx
|HTML5Rocks_link=
}}