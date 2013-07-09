{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|HTMLElement is the interface that all DOM Nodes subclass from. It provides functionality specific to HTML that is not present in the basic Element interface.}}
{{API_Object
|Subclass_of=dom/Element, dom/Node
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=All HTML element interfaces derive from this class.
|Import_Notes====Additional Members (MSDN)===
The '''HTMLElement''' object has these types of members:
[[#Additional_Events|Additional Events]]
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Events====
The '''HTMLElement''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[apis/audio-video/events/cuechange|'''oncuechange''']]
{{!}}Occurs when a [[apis/audio-video/TextTrackCue|'''TextTrackCue''']] in a '''HTMLTrackElement''' changes.
{{!}}-
{{!}}[[dom/events/mscontentzoom|'''onmscontentzoom''']]
{{!}}Event fires when a user zooms the element.
{{!}}-
{{!}}[[dom/events/msgesturechange|'''onmsgesturechange''']]
{{!}}Triggered when the finger positions associated with the interaction moves on the screen. It will also be triggered during  inertia processing.
{{!}}-
{{!}}[[dom/events/msgestureend|'''onmsgestureend''']]
{{!}}This event fires when all associated contacts are removed from the surface, and any inertia related movements have stopped..
{{!}}-
{{!}}[[dom/events/msgesturehold|'''onmsgesturehold''']]
{{!}}Fires when the user touches a surface and holds the position for an extended period of time.
{{!}}-
{{!}}[[dom/events/msgesturestart|'''onmsgesturestart''']]
{{!}}Triggered when the screen is touched on a location over this element.
{{!}}-
{{!}}[[dom/events/msgesturetap|'''onmsgesturetap''']]
{{!}}Triggers when user interaction of a touch, mouse click, or pen tap.
{{!}}-
{{!}}[[dom/events/msgotpointercapture|'''onmsgotpointercapture''']]
{{!}}Event that is fired when a pointer is captured to the element.
{{!}}-
{{!}}[[dom/events/msinertiastart|'''onmsinertiastart''']]
{{!}}Event fires once contact is removed when a move or pan has sufficient speed to continue moving.
{{!}}-
{{!}}[[dom/events/mslostpointercapture|'''onmslostpointercapture''']]
{{!}}Event that is triggered when the element loses a pointer capture.
{{!}}-
{{!}}[[dom/events/msmanipulationstatechanged|'''onmsmanipulationstatechanged''']]
{{!}}Event fires when the state of an element being manipulated has changed.
{{!}}-
{{!}}[[dom/events/mspointerdown|'''onmspointerdown''']]
{{!}}Event that is triggered when a contact touches the screen on element.
{{!}}-
{{!}}[[dom/events/mspointerhover|'''onmspointerhover''']]
{{!}}Event that is triggered when a contact (normally a pen) moves over an element without touching the surface.
{{!}}-
{{!}}[[dom/events/mspointermove|'''onmspointermove''']]
{{!}}Event that is triggered when a contact moves on the screen while over an element.
{{!}}-
{{!}}[[dom/events/mspointerout|'''onmspointerout''']]
{{!}}This event is triggered when a pointer moves from inside to outside the boundaries of this element. This event is always raised, whether or not the pointer is captured to this element.
{{!}}-
{{!}}[[dom/events/mspointerover|'''onmspointerover''']]
{{!}}Event that is triggered when a contact moves from outside to inside the bounds of this element. This event is always raised, whether or not the pointer is captured to this element.
{{!}}-
{{!}}[[dom/events/mspointerup|'''onmspointerup''']]
{{!}}Event that is triggered when a contact is raised off of the screen over an element.
{{!}}}
 

====Additional Methods====
The '''HTMLElement''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/msReleasePointerCapture|'''msReleasePointerCapture''']]
{{!}}Releases a pointer captured by an element.
{{!}}-
{{!}}[[dom/methods/msSetPointerCapture|'''msSetPointerCapture''']]
{{!}}Assigns the current pointer (touch, pen, or mouse) and [[dom/objects/MSPointerEvent|'''MSPointerEvents''']] to a specific element.
{{!}}}
 

====Additional Properties====
The '''HTMLElement''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/classList|'''classList''']]
{{!}}Returns a [[dom/DOMTokenList|'''DOMTokenList''']] that represents the [[dom/properties/className|'''className''']] attribute value expressed as a string.
{{!}}-
{{!}}[[dom/properties/spellcheck|'''spellcheck''']]
{{!}}Specifies whether spell checking is applied to an editable text field.
{{!}}}
 
{{Editorial/Merge_Candidate
|Other=dom/apis/HTMLElement
}}
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}