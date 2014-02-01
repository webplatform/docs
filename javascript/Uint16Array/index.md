{{Page_Title}}
{{Flags}}
{{Summary_Section|A typed array of 16-bit unsigned integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= uint16Array = new Uint16Array( length );}}{{JS_Syntax_Format
|Format= uint16Array = new Uint16Array( array );}}{{JS_Syntax_Format
|Format= uint16Array = new Uint16Array( buffer , byteOffset , length );}}
|Values={{JS_Syntax_Parameter
|Name=uint16Array
|Required=Required
|Description=The variable name to which the '''Uint16Array''' object is assigned.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=Specifies the length (in bytes) of the array.}}{{JS_Syntax_Parameter
|Name=array
|Required=
|Description=The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Uint16 type.}}{{JS_Syntax_Parameter
|Name=buffer
|Required=
|Description=The ArrayBuffer that the Uint16Array represents.}}{{JS_Syntax_Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the Uint16Array should begin.}}{{JS_Syntax_Parameter
|Name=length
|Required=
|Description=The length of the array.}}
}}
==Constants==
The following table lists the constants of the '''Uint16Array''' object.

{| class='wikitable'
|-
! Constant
! Description
|-
| [[javascript/Uint16Array/BYTES PER ELEMENT|BYTES_PER_ELEMENT Constant]]
| The size in bytes of each element in the array.
|}
==Properties==
The following table lists the constants of the '''Uint16Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Uint16Array/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this array.
|-
| [[javascript/Uint16Array/byteLength|byteLength Property]]
| Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Uint16Array/byteOffset|byteOffset Property]]
| Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Uint16Array/length|length Property]]
| The length of the array.
|}
==Methods==
The following table lists the methods of the '''Uint16Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Uint16Array/get|get Method]]
| Omittable. Gets the element at the specified index.
|-
| [[javascript/Uint16Array/set|set Method (Uint16Array)]]
| Sets a value or an array of values.
|-
| [[javascript/Uint16Array/subarray|subarray Method (Uint16Array)]]
| Gets a new Uint16Array view of the ArrayBuffer store for this array.
|}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use a Uint16Array object to process the binary data acquired from an XmlHttpRequest:

|Code= var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Uint16Array(buffer.byteLength / 2);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getUint16(i * 2);
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212484(v=vs.94).aspx
|HTML5Rocks_link=
}}