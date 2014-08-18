{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Sets a value or an array of values.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=int8Array.set(index, value);
}}{{JS Syntax Format
|Format=int8Array.set(array, offset);
}}
|Values={{JS Syntax Parameter
|Name=index
|Description=The index of the location to set.
}}{{JS Syntax Parameter
|Name=value
|Description=The value to set.
}}{{JS Syntax Parameter
|Name=array
|Description=A typed or untyped array of values to set.
}}{{JS Syntax Parameter
|Name=offset
|Description=The index in the current array at which the values are to be written.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to set the first element of the array.
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float64Array(buffer.byteLength / 8);
             floatArr.set(0, 9.1);
         }
     }
}}
}}
{{Remarks_Section
|Remarks=If the input array is a TypedArray, the two arrays may use the same underlying ArrayBuffer. In this situation, setting the values takes place as if all the data is first copied into a temporary buffer that does not overlap either of the arrays, and then the data from the temporary buffer is copied into the current array.

If the offset plus the length of the given array is out of range for the current TypedArray, an exception is raised.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212927(v=vs.94).aspx
|HTML5Rocks_link=
}}