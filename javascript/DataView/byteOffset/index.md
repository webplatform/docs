{{Page_Title}}
{{Flags}}
{{Summary_Section|Read-only. The offset of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arrayOffset = dataView.byteOffset;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the length of a DataView.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.byteOffset)
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212912(v=vs.94).aspx
|HTML5Rocks_link=
}}