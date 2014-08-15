{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|A typed array of 8-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=int8Array = new Int8Array( length );
}}{{JS Syntax Format
|Format=intArray = new IntArray( array );
}}{{JS Syntax Format
|Format=intArray = new IntArray( buffer , byteOffset , length );
}}
|Values={{JS Syntax Parameter
|Name=int8Array
|Required=Required
|Description=The variable name to which the '''Int8Array''' object is assigned.
}}{{JS Syntax Parameter
|Name=length
|Description=Specifies the length (in bytes) of the array.
}}{{JS Syntax Parameter
|Name=array
|Description=The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Int8 type.
}}{{JS Syntax Parameter
|Name=buffer
|Description=The ArrayBuffer that the Int8Array represents.
}}{{JS Syntax Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the Int8Array should begin.
}}{{JS Syntax Parameter
|Name=length
|Description=The length of the array.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use an Int8Array object to process the binary data acquired from an XmlHttpRequest:
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Int8Array(buffer.byteLength);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getInt8(i);
             }
         alert(ints[10]);
         }
     }
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
==Constants==
The following table lists the constants of the '''Int8Array''' object.

{| class='wikitable'
|-
! Constant
! Description
|-
| [[javascript/Int8Array/BYTES PER ELEMENT|BYTES_PER_ELEMENT Constant]]
| The size in bytes of each element in the array.
|}
==Properties==
The following table lists the constants of the '''Int8Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Int8Array/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this array.
|-
| [[javascript/Int8Array/byteLength|byteLength Property]]
| Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Int8Array/byteOffset|byteOffset Property]]
| Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Int8Array/length|length Property]]
| The length of the array.
|}
==Methods==
The following table lists the methods of the '''Int8Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Int8Array/get|get Method]]
| Omittable. Gets the element at the specified index.
|-
| [[javascript/Int8Array/set|set Method (Int8Array)]]
| Sets a value or an array of values.
|-
| [[javascript/Float64Array/subarray|subarray Method (Float64Array)]]
| Gets a new Int8Array view of the ArrayBuffer store for this array.
|}

{{Topics | JS Basic}}
{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212462(v=vs.94).aspx
|HTML5Rocks_link=
}}