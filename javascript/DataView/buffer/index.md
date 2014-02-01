{{Page_Title}}
{{Flags}}
{{Summary_Section|Read-only. Gets the ArrayBuffer that is referenced by this view.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arrayBuffer = dataView.buffer;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the length of the ArrayBuffer underlying the DataView.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.buffer.byteLength)
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br230733(v=vs.94).aspx
|HTML5Rocks_link=
}}