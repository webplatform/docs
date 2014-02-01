{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets a new Int8Array view of the ArrayBuffer store for this array, referencing the elements at begin, inclusive, up to end, exclusive.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= var newInt8Array = int8Array.subset(begin, end);}}
|Values={{JS_Syntax_Parameter
|Name=newInt8Array
|Required=
|Description=The subarray returned by this method.}}{{JS_Syntax_Parameter
|Name=begin
|Required=
|Description=The index of the beginning of the array.}}{{JS_Syntax_Parameter
|Name=end
|Required=
|Description=The index of the end of the array.}}
}}
{{Remarks_Section
|Remarks=If either begin or end is negative, it refers to an index from the end of the array, as opposed to from the beginning. If end is unspecified, the subarray contains all elements from begin to the end of the TypedArray. The range specified by the begin and end values is clamped to the valid index range for the current array. If the computed length of the new TypedArray would be negative, it is clamped to zero. The returned TypedArray will be of the same type as the array on which this method is invoked.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to get a subarray three elements long, starting with the first element of the array.

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int8Array(buffer.byteLength);
             var subArr = intArr.subarray(0, 2);
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