{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets a value or an array of values.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= int8Array.set(index, value);}}{{JS_Syntax_Format
|Format= int8Array.set(array, offset);}}
|Values={{JS_Syntax_Parameter
|Name=index
|Required=
|Description=The index of the location to set.}}{{JS_Syntax_Parameter
|Name=value
|Required=
|Description=The value to set.}}{{JS_Syntax_Parameter
|Name=array
|Required=
|Description=A typed or untyped array of values to set.}}{{JS_Syntax_Parameter
|Name=offset
|Required=
|Description=The index in the current array at which the values are to be written.}}
}}
{{Remarks_Section
|Remarks=If the input array is a TypedArray, the two arrays may use the same underlying ArrayBuffer. In this situation, setting the values takes place as if all the data is first copied into a temporary buffer that does not overlap either of the arrays, and then the data from the temporary buffer is copied into the current array.

If the offset plus the length of the given array is out of range for the current TypedArray, an exception is raised.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to set the first element of the array.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Uint32Array(buffer.byteLength / 4);
             intArr.set(0, 9);
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}