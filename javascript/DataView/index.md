{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|You can use a DataView object to read and write the different kinds of binary data to any location in the ArrayBuffer.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dataView = '''new DataView(''' DataView( buffer , byteOffset , byteLength ));
}}
|Values={{JS Syntax Parameter
|Name=dataView
|Required=Required
|Description=The variable name to which the '''DataView''' object is assigned.
}}{{JS Syntax Parameter
|Name=buffer
|Required=
|Description=The ArrayBuffer that the DataView represents.
}}{{JS Syntax Parameter
|Name=byteOffset
|Required=Optional
|Description=Specifies the offset in bytes from the start of the buffer at which the DataView should begin.
}}{{JS Syntax Parameter
|Name=byteLength
|Required=Optional
|Description=Specifies the length (in bytes) of the section of the buffer that the DataView should represent.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use a DataView object to process the binary data acquired from an XmlHttpRequest:
|Code=var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();
 
     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var ints = new Int32Array(dataView.byteLength / 4);
             for (var i = 0; i &lt; ints.length; i++) {
                 ints[i] = dataview.getInt32(i * 4);
             }
         alert(ints[10]);
         }
     }
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=If both byteOffset and byteLength are omitted, the DataView spans the entire ArrayBuffer range. If the byteLength is omitted, the DataView extends from the given byteOffset until the end of the ArrayBuffer. If the given byteOffset and byteLength references an area beyond the end of the ArrayBuffer, an exception is raised.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
==Properties==
The following table lists the properties of the '''DataView''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/DataView/buffer|buffer Property]]
| Read-only. Gets the ArrayBuffer that is referenced by this view.
|-
| [[javascript/DataView/byteLength|byteLength Property]]
| Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|-
| [[javascript/DataView/byteOffset|byteOffset Property]]
| Read-only. The offset of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.
|}
==Methods==
The following table lists the methods of the '''DataView''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/DataView/getInt8|getInt8 Method]]
| Gets the Int8 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getUint8|getUint8 Method (DataView)]]
| Gets the Uint8 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getInt16|getInt16 Method (DataView)]]
| Gets the Int16 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getUint16|getUint16 Method (DataView)]]
| Gets the Uint16 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getInt32|getInt32 Method (DataView)]]
| Gets the Int32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getUint32|getUint32 Method (DataView)]]
| Gets the Uint32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getFloat32|getFloat32 Method (DataView)]]
| Gets the Float32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/getFloat64|getFloat64 Method (DataView)]]
| Gets the Float64 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setInt8|setInt8 Method (DataView)]]
| Stores a Int8 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setUint8|setUint8 Method (DataView)]]
| Stores a Uint8 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setInt16|setInt16 Method (DataView)]]
| Stores a Int16 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setUint16|setUint16 Method (DataView)]]
| Stores a Uint16 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setInt32|setInt32 Method (DataView)]]
| Stores a Int32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setUint32|setUint32 Method (DataView)]]
| Stores a Uint32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setFloat32|setFloat32 Method (DataView)]]
| Stores a Float32 value at the specified byte offset from the start of the view.
|-
| [[javascript/DataView/setFloat64|setFloat64 Method (DataView)]]
| Stores a Float64 value at the specified byte offset from the start of the view.
|}

{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/br212463(v=vs.94).aspx
|HTML5Rocks_link=
}}