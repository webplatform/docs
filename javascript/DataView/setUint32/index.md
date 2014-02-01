{{Page_Title}}
{{Flags}}
{{Summary_Section|Sets the Uint32 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dataView.setUint32 (byteOffset, value, littleEndian); }}
|Values={{JS_Syntax_Parameter
|Name=byteOffset
|Required=
|Description=The place in the buffer at which the value should be retrieved.}}{{JS_Syntax_Parameter
|Name=value
|Required=
|Description=The value to set.}}{{JS_Syntax_Parameter
|Name=littleEndian
|Required=Optional
|Description=If false or undefined, a big-endian value should be written, otherwise a little-endian value should be written.}}
}}
{{Remarks_Section
|Remarks=These methods raise an exception if they would write beyond the end of the view.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to set the first Uint32 in the DataView.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setUint32(0, 9);
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212475(v=vs.94).aspx
|HTML5Rocks_link=
}}