{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
}}
{{Summary_Section|Represents a raw buffer of binary data, which is used to store data for the different typed arrays. ArrayBuffers cannot be read from or written to directly, but can be passed to a typed array or [[javascript/DataView{{!}}DataView Object]] to interpret the raw buffer as needed.

For more information about typed arrays, see Typed Arrays.
}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=arrayBuffer = new ArrayBuffer(length);
}}
|Values={{JS Syntax Parameter
|Name=arrayBuffer
|Required=Required
|Description=The variable name to which the '''ArrayBuffer''' object is assigned.
}}{{JS Syntax Parameter
|Name=length
|Description=The length of the buffer. The contents of the ArrayBuffer are initialized to 0. If the requested number of bytes could not be allocated an exception is raised.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use an ArrayBuffer object to process the binary data acquired from an XmlHttpRequest. You can use a [[javascript/DataView{{!}}DataView Object]] to get the individual values.
|Code=var req = new XMLHttpRequest();
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
}}
}}
{{Remarks_Section
|Remarks=For more information about using XmlHttpRequest , see XMLHttpRequest enhancements.
}}
{{Notes_Section}}
{{JS Object Listing}}
==Properties==
The following table lists the properties of the '''ArrayBuffer''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/ArrayBuffer/byteLength|byteLength Property]]
| Read-only. The length of the ArrayBuffer (in bytes).
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212474(v=vs.94).aspx
|HTML5Rocks_link=
}}