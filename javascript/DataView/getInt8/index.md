{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Gets the Int8 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=var testInt = dataView.getInt8(byteOffset);
}}
|Values={{JS Syntax Parameter
|Name=testInt
|Required=Required
|Description=The Int8 value that is returned from the method.
}}{{JS Syntax Parameter
|Name=byteOffset
|Required=
|Description=The place in the buffer at which the value should be retrieved.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to get the first Int8 in the DataView.
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.getInt8(0));
         }
     }
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=These methods raise an exception if they would read beyond the end of the view.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212471(v=vs.94).aspx
|HTML5Rocks_link=
}}