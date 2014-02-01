{{Page_Title}}
{{Flags}}
{{Summary_Section|A typed array of 32-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= uint32Array = new Uint32Array( length );}}{{JS_Syntax_Format
|Format= uint32Array = new Uint32Array( array );}}{{JS_Syntax_Format
|Format= uint32Array = new Uint32Array( buffer , byteOffset , length );}}
|Values={{JS_Syntax_Parameter
|Name=uint32Array
|Required=Required
|Description=The variable name to which the '''Uint32Array''' object is assigned.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=Specifies the length (in bytes) of the array.}}{{JS_Syntax_Parameter
|Name=array
|Required=
|Description=The array (or typed array) that is contained in this array. The contents are initialized to the contents of the given array or typed array, with each element converted to the Uint32 type.}}{{JS_Syntax_Parameter
|Name=buffer
|Required=
|Description=The ArrayBuffer that the Uint32Array represents.}}{{JS_Syntax_Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the Uint32Array should begin.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=The length of the array.}}
}}
==Constants==
The following table lists the constants of the '''Uint32Array''' object.

{| class='wikitable'
|-
! Constant
! Description
|-
| [[javascript/Uint32Array/BYTES PER ELEMENT|BYTES_PER_ELEMENT Constant]]
| The size in bytes of each element in the array.
|}
==Properties==
The following table lists the constants of the '''Uint32Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Uint32Array/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this array.
|-
| [[javascript/Uint32Array/byteLength|byteLength Property]]
| Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Uint32Array/byteOffset|byteOffset Property]]
| Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Uint32Array/length|length Property]]
| The length of the array.
|}
==Methods==
The following table lists the methods of the '''Uint32Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Uint32Array/get|get Method]]
| Omittable. Gets the element at the specified index.
|-
| [[javascript/Uint32Array/set|set Method (Uint32Array)]]
| Sets a value or an array of values.
|-
| [[javascript/Uint32Array/subarray|subarray Method (Uint32Array)]]
| Gets a new Uint32Array view of the ArrayBuffer store for this array.
|}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use a Uint32Array object to process the binary data acquired from an XMLHttpRequest:

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Uint32Array(buffer.byteLength / 4);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getUint32(i * 4);
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br230737(v=vs.94).aspx
|HTML5Rocks_link=
}}