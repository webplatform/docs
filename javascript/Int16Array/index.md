{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|A typed array of 16-bit integer values. The contents are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=int16Array = new Int16Array( length );
}}{{JS Syntax Format
|Format=int16Array = new Int16Array( array );
}}{{JS Syntax Format
|Format=int16Array = new Int16Array( buffer , byteOffset , length );
}}
|Values={{JS Syntax Parameter
|Name=int16Array
|Required=Required
|Description=The variable name to which the '''Int16Array''' object is assigned.
}}{{JS Syntax Parameter
|Name=length
|Description=Specifies the length (in bytes) of the array.
}}{{JS Syntax Parameter
|Name=array
|Description=The array (or typed array) that is contained in this array.. The contents are initialized to the contents of the given array or typed array, with each element converted to the Int16 type.
}}{{JS Syntax Parameter
|Name=buffer
|Description=The ArrayBuffer that the Int16Array represents.
}}{{JS Syntax Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the Int16Array should begin.
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
|Description=The following example shows how to use an Int16Array object to process the binary data acquired from an XmlHttpRequest:
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataview = new DataView(buffer);
             var ints = new Int16Array(buffer.byteLength / 2);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getInt16(i * 2);
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
The following table lists the constants of the '''Int16Array''' object.

{| class='wikitable'
|-
! Constant
! Description
|-
| [[javascript/Int16Array/BYTES PER ELEMENT|BYTES_PER_ELEMENT Constant]]
| The size in bytes of each element in the array.
|}
==Properties==
The following table lists the constants of the '''Int16Array''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Int16Array/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this array.
|-
| [[javascript/Int16Array/byteOffset|byteLength Property]]
| Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Int8Array/byteOffset|byteOffset Property]]
| Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/Float32Array/length|length Property]]
| The length of the array.
|}
==Methods==
The following table lists the methods of the '''Int16Array''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Int16Array/get|get Method]]
| Omittable. Gets the element at the specified index.
|-
| [[javascript/Int16Array/set|set Method (Int16Array)]]
| Sets a value or an array of values.
|-
| [[javascript/Int16Array/subarray|subarray Method (Int16Array)]]
| Gets a new Int16Array view of the ArrayBuffer store for this array.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212480(v=vs.94).aspx
|HTML5Rocks_link=
}}