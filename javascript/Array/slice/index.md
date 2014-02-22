{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a section of an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayObj.slice( start , [ end ])
}}
|Values={{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=An '''Array''' object.
}}{{JS Syntax Parameter
|Name=start
|Required=Required
|Description=The beginning of the specified portion of arrayObj.
}}{{JS Syntax Parameter
|Name=end
|Required=Optional
|Description=The end of the specified portion of arrayObj.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples show how to use the slice method. In the first example, all but the last element of <code>myArray</code> is copied into <code>newArray</code>. In the second example, only the last two elements of <code>myArray</code> are copied into <code>newArray</code>.
|Code=var origArray = [3, 5, 7, 9];
 var newArray = origArray.slice(0, -1);
 document.write(origArray);
 document.write("&lt;br/&gt;");
 newArray = origArray.slice(-2);
 document.write(newArray);
 
 // Output:
 // 3,5,7,9
 // 7,9
}}
}}
{{Remarks_Section
|Remarks=The '''slice''' method returns an '''Array''' object containing the specified portion of arrayObj.

The '''slice''' method copies up to, but not including, the element indicated by end. If start is negative, it is treated as length + start , where length is the length of the array. If end is negative, it is treated as length + end where length is the length of the array. If end is omitted, extraction continues to the end of arrayObj. If end occurs before start , no elements are copied to the new array.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/String/slice{{!}}slice Method (String)]]
* [[javascript/String{{!}}String Object]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/tkcsy6fe(v=vs.94).aspx
|HTML5Rocks_link=
}}