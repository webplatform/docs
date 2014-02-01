{{Page_Title}}
{{Flags}}
{{Summary_Section|Reverses the elements in an '''Array'''.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= arrayObj.reverse() }}
|Values={{JS_Syntax_Parameter
|Name=arrayObj
|Required=Required
|Description=Any '''Array''' object.}}
}}
{{JS_Return_Value
|Description=The reversed array.}}
{{Remarks_Section
|Remarks=The required arrayObj reference is an '''Array''' object.

The '''reverse''' method reverses the elements of an '''Array''' object in place. It does not create a new '''Array''' object during execution.

If the array is not contiguous, the '''reverse''' method creates elements in the array that fill the gaps in the array. Each of these created elements has the value undefined.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''reverse''' method.

|Code= var arr = new Array(0,1,2,3,4); 
 var reverseArr = arr.reverse();
 document.write(reverseArr);
 
 // Output:
 // 4,3,2,1,0
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/concat{{!}}concat Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/3333858x(v=vs.94).aspx
|HTML5Rocks_link=
}}