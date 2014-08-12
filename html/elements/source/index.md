{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add example.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Allows developer to specify multiple alternative media resources for media elements, such as <code><video></code> and <code><audio></code>. It does not represent anything on its own, and is used with <code>src</code> attribute to specify the URL.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  If you change the media file using the [[apis/audio-video/properties/src|'''src''']] property on an '''audio''' or '''video''' object, you need to call the [[apis/audio-video/methods/load|'''load''']] method before calling the [[apis/audio-video/methods/play|'''play''']] method. If you change the '''src''' and call the play() method without loading first, it will continue to play the file specified by the '''source''' element.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.8


===Members===
The '''source''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''source''' object has these events.
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
|[[apis/audio-video/events/canplay|'''oncanplay''']]
|Occurs when playback is possible, but would require further buffering.
|-
|[[apis/audio-video/events/canplaythrough|'''oncanplaythrough''']]
|Occurs when playback to end is possible without requiring a stop for further buffering.
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
|[[apis/audio-video/events/durationchange|'''ondurationchange''']]
|Occurs when the [[apis/audio-video/properties/duration|'''duration''']] attribute is updated.
|-
|[[apis/audio-video/events/emptied|'''onemptied''']]
|Occurs when the media element is reset to its initial state.
|-
|[[apis/audio-video/events/ended|'''onended''']]
|Occurs when the end of playback is reached.
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
|[[apis/audio-video/events/loadeddata|'''onloadeddata''']]
|Occurs when media data is loaded at the current playback position.
|-
|[[apis/audio-video/events/loadedmetadata|'''onloadedmetadata''']]
|Occurs when the duration and dimensions of the media have been determined.
|-
|[[apis/audio-video/events/loadstart|'''onloadstart''']]
|Occurs when Internet Explorer begins looking for media data.
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
|[[apis/audio-video/events/pause|'''onpause''']]
|Occurs when playback is paused.
|-
|[[apis/audio-video/events/play|'''onplay''']]
|Occurs when the [[apis/audio-video/methods/play|'''play''']] method is requested.
|-
|[[apis/audio-video/events/playing|'''onplaying''']]
|Occurs when the audio or video has started playing.
|-
|[[apis/audio-video/events/progress|'''onprogress''']]
|Occurs to indicate progress while downloading media data.
|-
|[[apis/audio-video/events/ratechange|'''onratechange''']]
|Occurs when the playback rate is increased or decreased.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[apis/audio-video/events/seeked|'''onseeked''']]
|Occurs when the seek operation ends.
|-
|[[apis/audio-video/events/seeking|'''onseeking''']]
|Occurs when the current playback position is moved.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|-
|[[apis/audio-video/events/stalled|'''onstalled''']]
|Occurs when the download has stopped.
|-
|[[apis/audio-video/events/suspend|'''onsuspend''']]
|Occurs if the load operation has been intentionally halted.
|-
|[[apis/audio-video/events/timeupdate|'''ontimeupdate''']]
|Occurs to indicate the current playback position.
|-
|[[apis/audio-video/events/volumechange|'''onvolumechange''']]
|Occurs when the volume is changed, or playback is muted or unmuted.
|-
|[[apis/audio-video/events/waiting|'''onwaiting''']]
|Occurs when playback stops because the next frame of a video resource is not available.
|}
 

====Methods====
The '''source''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/compareDocumentPosition|'''compareDocumentPosition''']]
|Compares the position of two nodes in a document.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
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
|[[dom/methods/isDefaultNamespace|'''isDefaultNamespace''']]
|Indicates whether or not a namespace is the default namespace for a document.
|-
|[[dom/methods/isEqualNode|'''isEqualNode''']]
|Determines if two nodes are equal.
|-
|[[dom/methods/isSameNode|'''isSameNode''']]
|Determines if two node references refer to the same node.
|-
|[[dom/methods/isSupported|'''isSupported''']]
|Returns a value indicating whether or not the object supports a specific DOM standard.
|-
|[[dom/methods/lookupNamespaceURI|'''lookupNamespaceURI''']]
|Gets the URI of the namespace associated with a namespace prefix, if any.
|-
|[[dom/methods/lookupPrefix|'''lookupPrefix''']]
|Gets the namespace prefix associated with a URI, if any.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|}
 

====Properties====
The '''source''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/media|'''media''']]
|Gets or sets the intended media type of the media source.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
|-
|[[dom/properties/prefix|'''prefix''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/src|'''src''']]
|The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
|-
|[[dom/properties/textContent|'''textContent''']]
|Sets or retrieves the text content of an object and any child objects.
|-
|[[apis/audio-video/properties/type|'''type''']]
|Gets or sets the MIME type of a media resource.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>audio</code>
*<code>video</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}