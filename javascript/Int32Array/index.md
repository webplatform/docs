{{Page_Title}}
{{Flags}}
{{Summary_Section|A typed array of 32-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= int32Array = new Int32Array( length );}}{{JS_Syntax_Format
|Format= int32Array = new Int32Array( array );}}{{JS_Syntax_Format
|Format= int32Array = new Int32Array( buffer , byteOffset , length );}}
|Values={{JS_Syntax_Parameter
|Name=int32Array
|Required=Required
|Description=The variable name to which the '''Int32Array''' object is assigned.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=Specifies the length (in bytes) of the array.}}{{JS_Syntax_Parameter
|Name=array
|Required=
|Description=The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Int32 type.}}{{JS_Syntax_Parameter
|Name=buffer
|Required=
|Description=The ArrayBuffer that the Int32Array represents.}}{{JS_Syntax_Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the Int32Array should begin.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=The length of the array.}}
}}
==Constants==
The following table lists the constants of the '''Int32Array''' object.

{| class='wikitable'
|-
! Constant
! Description
|-
| [[javascript/Int32Array/BYTES PER ELEMENT|BYTES_PER_ELEMENT Constant]]
| The size in bytes of each element in the array.
|}
==Properties==
The following table lists the constants of the '''Int32Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Int32Array/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this array.
|-
| [[javascript/Int32Array/byteLength|byteLength Property]]
| Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Int32Array/byteOffset|byteOffset Property]]
| Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Float32Array/length|length Property]]
| The length of the array.
|}
==Methods==
The following table lists the methods of the '''Int32Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Int32Array/get|Get Method]]
| Omittable. Gets the element at the specified index.
|-
| [[javascript/Int32Array/set|set Method (Int32Array)]]
| Sets a value or an array of values.
|-
| [[javascript/Int32Array/subarray|subarray Method (Int32Array)]]
| Gets a new Int32Array view of the ArrayBuffer store for this array.
|}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use an Int32Array object to process the binary data acquired from an XmlHttpRequest:

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Int32Array(buffer.byteLength / 4);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getInt32(i * 4);
             }
         alert(ints[10]);
         }
     }
}}}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212468(v=vs.94).aspx
|HTML5Rocks_link=
}}