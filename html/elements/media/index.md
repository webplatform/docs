{{Page_Title}}
{{Flags
|Checked_Out=true
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Presents audio or video data to the user. The media element provides the [[html/elements/audio|audio]] and [[html/elements/video|video]] objects which are used to play sound and video content.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10


===Members===
The '''media''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''media''' object has these events.
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
|[[dom/events/drop|'''ondrop''']]
|Fires on the target object when the mouse button is released during a drag-and-drop operation.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/focus|'''onfocus''']]
|Fires when the object receives focus.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
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
The '''media''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/audio-video/methods/canPlayType|'''canPlayType''']]
|Returns a string that specifies whether the client can play a given media resource type.
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
|[[apis/audio-video/methods/load|'''load''']]
|Resets the '''IHTMLMediaElement''' and loads a new media resource.
|-
|[[dom/methods/lookupNamespaceURI|'''lookupNamespaceURI''']]
|Gets the URI of the namespace associated with a namespace prefix, if any.
|-
|[[dom/methods/lookupPrefix|'''lookupPrefix''']]
|Gets the namespace prefix associated with a URI, if any.
|-
|'''msClearEffects'''
|Clears all effects from the media pipeline.
|-
|'''msInsertAudioEffect'''
|Inserts the specified audio effect into media pipeline.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|'''msSetMediaProtectionManager'''
|Specifies the media protection manager for a given media pipeline.
|-
|[[apis/audio-video/methods/pause|'''pause''']]
|Pauses the current playback and sets [[apis/audio-video/properties/paused|'''paused''']] to TRUE.
|-
|[[apis/audio-video/methods/play|'''play''']]
|Loads and starts playback of a media resource.
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
The '''media''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[apis/audio-video/properties/audioTracks|'''audioTracks''']]
|Returns an [[apis/audio-video/AudioTrackList|'''AudioTrackList''']] object with the audio tracks for a given '''video''' element.
|-
|[[apis/audio-video/properties/autobuffer|'''autobuffer''']]
|The [[apis/audio-video/properties/autobuffer|'''autobuffer''']] element is not supported by Internet Explorer 9. Use the [[apis/audio-video/properties/preload|'''preload''']] element instead.

This property is not supported for Metro style apps using JavaScript
|-
|[[apis/audio-video/properties/autoplay|'''autoplay''']]
|Gets or sets a value that indicates whether to start playing the media automatically.
|-
|[[apis/audio-video/properties/buffered|'''buffered''']]
|Gets a collection of buffered time ranges.
|-
|[[apis/audio-video/properties/controls|'''controls''']]
|Gets or sets a flag that indicates whether the client provides a set of controls for the media (in case the developer does not include controls for the player).
|-
|[[apis/audio-video/properties/currentSrc|'''currentSrc''']]
|Gets the address or URL of the current media resource ('''video''','''audio''') that is selected by '''IHTMLMediaElement'''.
|-
|[[apis/audio-video/properties/currentTime|'''currentTime''']]
|Gets or sets the current playback position, in seconds.
|-
|[[apis/audio-video/properties/defaultPlaybackRate|'''defaultPlaybackRate''']]
|Gets or sets the default playback rate when the user is not using fast foward or reverse for a video or audio resource.
|-
|[[apis/audio-video/properties/duration|'''duration''']]
|Gets the duration, in seconds, of the current media resource, a <code>NaN</code> value if duration is not available, or <code>Infinity</code> if the media resource is streaming.
|-
|[[apis/audio-video/properties/ended|'''ended''']]
|Gets information about whether the playback has ended or not.
|-
|[[apis/audio-video/properties/error|'''error''']]
|Gets an '''IHTMLMediaError''' object representing the current error state of the media element.
|-
|[[apis/audio-video/properties/initialTime|'''initialTime''']]
|Gets the earliest possible position, in seconds, that the playback can begin.
|-
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/loop|'''loop''']]
|Gets or sets a flag that specifies whether playback should restart after it completes.
|-
|'''msAudioCategory'''
|Specifies the purpose of the audio or video media, such as background audio or alerts.
|-
|'''msAudioDeviceType'''
|Specifies the output device id that the audio will be sent to.
|-
|'''msPlayToDisabled'''
|Gets or sets whether the DLNA PlayTo device is available.
|-
|'''msPlayToPrimary'''
|Gets or sets the primary DLNA PlayTo device.
|-
|'''msPlayToSource'''
|Gets the source associated with the media element for use by the PlayToManager.
|-
|'''msRealTime'''
|Specifies whether or not to enable low-latency playback on the media element.
|-
|[[apis/audio-video/properties/muted|'''muted''']]
|Gets or sets a flag that indicates whether the audio (either audio or the audio track on video media) is muted.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/networkState|'''networkState''']]
|Gets the current network activity for the element.
|-
|[[apis/audio-video/properties/paused|'''paused''']]
|Gets a flag that specifies whether playback is paused.
|-
|[[apis/audio-video/properties/playbackRate|'''playbackRate''']]
|Gets or sets the current speed for the media resource to play. This speed is expressed as a multiple of the normal speed of the media resource.
|-
|[[apis/audio-video/properties/played|'''played''']]
|Gets [[apis/audio-video/HTMLTimeRanges|'''TimeRanges''']] for the current media resource that has been played.
|-
|[[dom/properties/prefix|'''prefix''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[apis/audio-video/properties/preload|'''preload''']]
|Gets or sets a hint to how much buffering is advisable for a media resource, even if [[apis/audio-video/properties/autoplay|'''autoplay''']] is not specified.
|-
|[[apis/audio-video/properties/seekable|'''seekable''']]
|Returns a [[apis/audio-video/HTMLTimeRanges|'''TimeRanges''']] object that represents the ranges of the current media resource that can be seeked.
|-
|[[apis/audio-video/properties/seeking|'''seeking''']]
|Gets a flag that indicates whether the the client is currently moving to a new playback position in the media resource.
|-
|[[apis/audio-video/properties/src|'''src''']]
|The address or URL of the a media resource ('''video''', '''audio''') that is to be considered.
|-
|[[dom/properties/textContent|'''textContent''']]
|Sets or retrieves the text content of an object and any child objects.
|-
|[[apis/audio-video/properties/volume|'''volume''']]
|Gets or sets the volume level for audio portions of the media element.
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
*<code>Reference</code>
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