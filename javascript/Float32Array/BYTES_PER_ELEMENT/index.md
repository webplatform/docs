{{Page_Title}}
{{Flags}}
{{Summary_Section|The size in bytes of each element in the array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var arraySize = int8Array.BYTES_PER_ELEMENT;}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the size of the array elements.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float32Array(buffer.byteLength / 4);
             alert(floatArr.BYTES_PER_ELEMENT);
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