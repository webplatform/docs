{{Page_Title}}
{{Flags}}
{{Summary_Section|Removes the first element from an array and returns it.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= arrayObj.shift( )}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required arrayObj reference is an '''Array''' object.}}
}}
{{JS_Return_Value
|Description=Returns the element removed from the array.}}
{{Remarks_Section
|Remarks=The following example illustrates the use of the shift method.

 var arr = new Array(10, 11, 12);
 while (arr.length &gt; 0)
     {
     var i = arr.shift();
     document.write (i.toString() + " ");
     }
 
 // Output: 
 // 10 11 12
}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/unshift{{!}}unshift Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9e7b4w20(v=vs.94).aspx
|HTML5Rocks_link=
}}