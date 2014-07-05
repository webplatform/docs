{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
}}
{{Summary_Section|Sets the Float64 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dataView.setFloat64 (byteOffset, value, littleEndian);
}}
|Values={{JS Syntax Parameter
|Name=byteOffset
|Description=The place in the buffer at which the value should be retrieved.
}}{{JS Syntax Parameter
|Name=value
|Description=The value to set.
}}{{JS Syntax Parameter
|Name=littleEndian
|Required=Optional
|Description=If false or undefined, a big-endian value should be written, otherwise a little-endian value should be written.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to set the first Float64 in the DataView.
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setFloat64(0, 9.1);
         }
     }
}}
}}
{{Remarks_Section
|Remarks=These methods raise an exception if they would write beyond the end of the view.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212469(v=vs.94).aspx
|HTML5Rocks_link=
}}