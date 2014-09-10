{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Move_Candidate
| Probably should be under HTML5 canvas element. See [http://www.w3.org/html/wg/drafts/html/master/single-page.html#the-canvas-element HTML5 specification].
}}
|Checked_Out=No
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The surface on which to apply graphics and images. The canvas object must contain an graphic created with [[canvas/objects/CanvasRenderingContext2D|'''CanvasRenderingContext2D''']] APIs 
in order to render. When the actual drawing is done using the '''CanvasRenderingContext2D''' object, the properties and methods are used to create and manipulate graphics on a canvas object.
}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10


===Members===
The '''canvas''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''canvas''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/blur|'''onblur''']]
|Fires when the object loses the input focus.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/drag|'''ondrag''']]
|Fires on the source object continuously during a drag operation.
|-
|[[dom/events/dragend|'''ondragend''']]
|Fires on the source object when the user releases the mouse at the close of a drag operation.
|-
|[[dom/events/dragenter|'''ondragenter''']]
|Fires on the target element when the user drags the object to a valid drop target.
|-
|[[dom/events/dragleave|'''ondragleave''']]
|Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
|-
|[[dom/events/dragover|'''ondragover''']]
|Fires on the target element continuously while the user drags the object over a valid drop target.
|-
|[[dom/events/dragstart|'''ondragstart''']]
|Fires on the source object when the user starts to drag a text selection or selected object.
|-
|[[dom/events/drop|'''ondrop''']]
|Fires on the target object when the mouse button is released during a drag-and-drop operation.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/focus|'''onfocus''']]
|Fires when the object receives focus.
|-
|[[dom/events/focusin|'''onfocusin''']]
|Fires for an element just prior to setting focus on that element.
|-
|[[dom/events/focusout|'''onfocusout''']]
|Fires for the current element with focus immediately after moving focus to another element.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/keydown|'''onkeydown''']]
|Fires when the user presses a key.
|-
|[[dom/events/keypress|'''onkeypress''']]
|Fires when the user presses an alphanumeric key.
|-
|[[dom/events/keyup|'''onkeyup''']]
|Fires when the user releases a key.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[dom/events/mousedown|'''onmousedown''']]
|Fires when the user clicks the object with either mouse button.
|-
|[[dom/events/mousemove|'''onmousemove''']]
|Fires when the user moves the mouse over the object.
|-
|[[dom/events/mouseout|'''onmouseout''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mouseover|'''onmouseover''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseup|'''onmouseup''']]
|Fires when the user releases a mouse button while the mouse is over the object.
|-
|[[dom/events/mousewheel|'''onmousewheel''']]
|Fires when the wheel button is rotated.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[dom/events/scroll|'''onscroll''']]
|Fires when the user repositions the scroll box in the scroll bar on the object.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|}
 

====Methods====
The '''canvas''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[canvas/methods/getContext|'''getContext''']]
|Returns an object that provides methods and properties for drawing and manipulating images and graphics on a '''canvas''' element in a document.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[canvas/methods/msToBlob|'''msToBlob''']]
|Returns a [[apis/file/Blob|'''blob object''']] from a canvas image or drawing.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|-
|[[canvas/methods/toDataURL|'''toDataURL''']]
|Returns the content of the current canvas as an image that  you can  use as  a source for another canvas or an HTML element (such as '''img''').
|}
 

====Properties====
The '''canvas''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[canvas/properties/height (canvas)|'''height''']]
|Gets or sets the height of a '''canvas''' element on a document.
|-
|[[canvas/properties/width (canvas)|'''width''']]
|Gets or sets the width of a '''canvas''' element on a document.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic support
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Hardware accelerated canvas
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}