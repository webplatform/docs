{{Page_Title}}
{{Flags}}
{{Summary_Section|Read-only. The length of the ArrayBuffer (in bytes).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arrayLength = arrayBuffer.byteLength;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the byte length of the ArrayBuffer.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
 
         alert(buffer.byteLength);
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212482(v=vs.94).aspx
|HTML5Rocks_link=
}}