{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Appends new elements to an array, and returns the new length of the array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayObj.push([ item1  [ item2 [. . . [ itemN ]]]])
}}
|Values={{JS Syntax Parameter
|Name=arrayObj
|Required=Required
|Description=An '''Array''' object.
}}{{JS Syntax Parameter
|Name=item, item2,. . ., itemN
|Required=Optional
|Description=New elements of the '''Array'''.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''push''' method.
|Code=var number;
 var my_array = new Array();
 
 my_array.push (5, 6, 7);
 my_array.push (8, 9);
 
 number = my_array.pop();
 while (number != undefined)
    {
    document.write (number + " ");
    number = my_array.pop();
    }
 
 // Output:
 // 9 8 7 6 5
}}
}}
{{Remarks_Section
|Remarks=The '''push''' and '''pop''' methods allow you to simulate a last in, first out stack.

The '''push''' method appends elements in the order in which they appear. If one of the arguments is an array, it is added as a single element. Use the '''concat''' method to join the elements from two or more arrays.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array/concat{{!}}concat Method (Array)]]
* [[javascript/Array/pop{{!}}pop Method (Array)]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/6d0cbb1w(v=vs.94).aspx
|HTML5Rocks_link=
}}