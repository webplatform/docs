{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the Float64 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var testFloat = dataView.getFloat64(byteOffset, littleEndian); }}
|Values={{JS_Syntax_Parameter
|Name=testFloat
|Required=Required
|Description=The Float64 value that is returned from the method.}}{{JS_Syntax_Parameter
|Name=byteOffset
|Required=
|Description=The place in the buffer at which the value should be retrieved.}}{{JS_Syntax_Parameter
|Name=littleEndian
|Required=Optional
|Description=If false or undefined, a big-endian value should be read, otherwise a little-endian value should be read.}}
}}
{{Remarks_Section
|Remarks=These methods raise an exception if they would read beyond the end of the view.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the first Float64 in the DataView.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.getFloat64(0));
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212466(v=vs.94).aspx
|HTML5Rocks_link=
}}