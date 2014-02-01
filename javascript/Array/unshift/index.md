{{Page_Title}}
{{Flags}}
{{Summary_Section|Inserts new elements at the start of an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= arrayObj.unshift([ item1 [, item2 [, . . . [, itemN]]]])}}
|Values={{JS_Syntax_Parameter
|Name=arrayObj
|Required=Required
|Description=An '''Array''' object.}}{{JS_Syntax_Parameter
|Name=item1, item2,. . ., itemN
|Required=Optional
|Description=Elements to insert at the start of the '''Array'''.}}
}}
{{Remarks_Section
|Remarks=The '''unshift''' method inserts elements into the start of an array, so they appear in the same order in which they appear in the argument list.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the unshift method.

|Code= var ar = new Array();
 ar.unshift(10, 11);
 ar.unshift(12, 13, 14);
 document.write(ar.toString());
 
 // Output: 12,13,14,10,11
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/shift{{!}}shift Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ezk94dwt(v=vs.94).aspx
|HTML5Rocks_link=
}}