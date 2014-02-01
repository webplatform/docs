{{Page_Title}}
{{Flags}}
{{Summary_Section|Omittable. Gets the element at the specified index.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var value = int32Array.get(index);}}
|Values={{JS_Syntax_Parameter
|Name=value
|Required=
|Description=The value returned by this method.}}{{JS_Syntax_Parameter
|Name=index
|Required=
|Description=The index at which to get the element of the array.}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get the first element of the array.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int32Array(buffer.byteLength / 4);
             var element = intArr.get(0);
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