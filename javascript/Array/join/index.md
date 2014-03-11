{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Adds all the elements of an array separated by the specified separator string.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=join([ separator ])
}}
|Values={{JS Syntax Parameter
|Name=separator
|Required=Optional
|Description=A string used to separate one element of an array from the next in the resulting String. If omitted, the array elements are separated with a comma.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''join''' method.
|Code=var a, b;
 a = new Array(0,1,2,3,4);
 b = a.join( "-" ) ;
 document.write(b);
 
 // Output:
 // 0-1-2-3-4
}}
}}
{{Remarks_Section
|Remarks=If any element of the array is '''undefined''' or null , it is treated as an empty string.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/String{{!}}String Object]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/59x7k999(v=vs.94).aspx
|HTML5Rocks_link=
}}