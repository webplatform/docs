{{Page_Title}}
{{Flags}}
{{Summary_Section|Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arrayOffset = uint16Array.byteOffset;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the offset of the array.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Uint16Array(buffer.byteLength / 2);
             alert(intArr.byteOffset);
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