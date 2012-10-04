{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
All HTML element interfaces derive from this class.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_htmlref\ie]:%20HTMLElement object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Members===
The '''HTMLElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''HTMLElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[apis/audio-video/events/cuechange|'''oncuechange''']]
|Occurs when a [[apis/audio-video/TextTrackCue|'''TextTrackCue''']] in a '''HTMLTrackElement''' changes.
|-
|[[dom/events/mscontentzoom|'''onmscontentzoom''']]
|Event fires when a user zooms the element.
|-
|[[dom/events/msgesturechange|'''onmsgesturechange''']]
|Triggered when the finger positions associated with the interaction moves on the screen. It will also be triggered during  inertia processing.
|-
|[[dom/events/msgestureend|'''onmsgestureend''']]
|This event fires when all associated contacts are removed from the surface, and any inertia related movements have stopped..
|-
|[[dom/events/msgesturehold|'''onmsgesturehold''']]
|Fires when the user touches a surface and holds the position for an extended period of time.
|-
|[[dom/events/msgesturestart|'''onmsgesturestart''']]
|Triggered when the screen is touched on a location over this element.
|-
|[[dom/events/msgesturetap|'''onmsgesturetap''']]
|Triggers when user interaction of a touch, mouse click, or pen tap.
|-
|[[dom/events/msgotpointercapture|'''onmsgotpointercapture''']]
|Event that is fired when a pointer is captured to the element.
|-
|[[dom/events/msinertiastart|'''onmsinertiastart''']]
|Event fires once contact is removed when a move or pan has sufficient speed to continue moving.
|-
|[[dom/events/mslostpointercapture|'''onmslostpointercapture''']]
|Event that is triggered when the element loses a pointer capture.
|-
|[[dom/events/msmanipulationstatechanged|'''onmsmanipulationstatechanged''']]
|Event fires when the state of an element being manipulated has changed.
|-
|[[dom/events/mspointerdown|'''onmspointerdown''']]
|Event that is triggered when a contact touches the screen on element.
|-
|[[dom/events/mspointerhover|'''onmspointerhover''']]
|Event that is triggered when a contact (normally a pen) moves over an element without touching the surface.
|-
|[[dom/events/mspointermove|'''onmspointermove''']]
|Event that is triggered when a contact moves on the screen while over an element.
|-
|[[dom/events/mspointerout|'''onmspointerout''']]
|This event is triggered when a pointer moves from inside to outside the boundaries of this element. This event is always raised, whether or not the pointer is captured to this element.
|-
|[[dom/events/mspointerover|'''onmspointerover''']]
|Event that is triggered when a contact moves from outside to inside the bounds of this element. This event is always raised, whether or not the pointer is captured to this element.
|-
|[[dom/events/mspointerup|'''onmspointerup''']]
|Event that is triggered when a contact is raised off of the screen over an element.
|}
 

====Methods====
The '''HTMLElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/msReleasePointerCapture|'''msReleasePointerCapture''']]
|Releases a pointer captured by an element.
|-
|[[dom/methods/msSetPointerCapture|'''msSetPointerCapture''']]
|Assigns the current pointer (touch, pen, or mouse) and [[dom/objects/MSPointerEvent|'''MSPointerEvents''']] to a specific element.
|}
 

====Properties====
The '''HTMLElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/classList|'''classList''']]
|Returns a [[dom/DOMTokenList|'''DOMTokenList''']] that represents the [[dom/properties/className|'''className''']] attribute value expressed as a string.
|-
|[[html/attributes/draggable|'''draggable''']]
|Sets or gets whether an element can be dragged on a document.
|-
|[[dom/properties/spellcheck|'''spellcheck''']]
|Specifies whether spell checking is applied to an editable text field.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}