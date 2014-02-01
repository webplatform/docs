{{Page_Title}}
{{Flags}}
{{Summary_Section|Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arrayByteLength = uint32Array.byteLength;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the length of the array.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Uint32Array(buffer.byteLength / 4);
             alert(intArr.byteLength);
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