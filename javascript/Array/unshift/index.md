{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Inserts new elements at the start of an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=unshift([ item1 [, item2 [, . . . [, itemN]]]])
}}
|Values={{JS Syntax Parameter
|Name=item1, item2,. . ., itemN
|Required=Optional
|Description=Elements to insert at the start of the '''Array'''.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the unshift method.
|Code=var ar = new Array();
 ar.unshift(10, 11);
 ar.unshift(12, 13, 14);
 document.write(ar.toString());
 
 // Output: 12,13,14,10,11
}}
}}
{{Remarks_Section
|Remarks=The '''unshift''' method inserts elements into the start of an array, so they appear in the same order in which they appear in the argument list.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array/shift{{!}}shift Method (Array)]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ezk94dwt(v=vs.94).aspx
|HTML5Rocks_link=
}}