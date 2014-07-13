{{Page_Title|initPointerEvent}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Flags, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new [[dom/PointerEvent|PointerEvent]] created by the [[dom/Document/createEvent|createEvent]] method.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=type
|Data type=String
|Description=The type of the event being created, such as: pointerdown, pointerup, pointercancel, pointermove, pointerover, pointerout, pointerenter, pointerleave, gotpointercapture, lostpointercapture.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Indicates whether the event can bubble.
When true, the event should propagate upward. 
When false, the event does not propagate upward.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Indicates whether the event’s default action can be prevented.
When true, the default action can be canceled. 
When false, the default action cannot be canceled.
|Optional=No
}}{{Method Parameter
|Name=view
|Data type=any
|Description=The view in which the event is taking place.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies some detailed information depending upon the event.
|Optional=No
}}{{Method Parameter
|Name=screenX
|Data type=Number
|Description=The x-coordinate of the event in screen coordinates relative to the upper left corner of the screen.
|Optional=No
}}{{Method Parameter
|Name=screenY
|Data type=Number
|Description=The y-coordinate of the event in screen coordinates relative to the upper left corner of the screen.
|Optional=No
}}{{Method Parameter
|Name=clientX
|Data type=Number
|Description=The x-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.
|Optional=No
}}{{Method Parameter
|Name=clientY
|Data type=Number
|Description=The y-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.
|Optional=No
}}{{Method Parameter
|Name=ctrlKey
|Data type=Boolean
|Description=Indicates the state of the Ctrl key.
When true, the left or right Ctrl key is pressed. 
If false, neither Ctrl key is pressed.
|Optional=No
}}{{Method Parameter
|Name=altKey
|Data type=Boolean
|Description=Indicates the state of the Alt key.
When true, the left or right Alt key is pressed. 
If false, neither Alt key is pressed.
|Optional=No
}}{{Method Parameter
|Name=shiftKey
|Data type=Boolean
|Description=Indicates the state of the Shift key.
When true, the left or right Shift key is pressed. 
If false, neither Shift key is pressed.
|Optional=No
}}{{Method Parameter
|Name=metaKey
|Data type=Boolean
|Description=Indicates the state of the Meta/Command key.
If true, the left or right Meta/Command key is pressed. 
If false
neither Meta/Command key is pressed.
|Optional=No
}}{{Method Parameter
|Name=button
|Data type=Number
|Description=If the event is caused by a mouse event, this indicates the mouse button that caused the event.
|Optional=No
}}{{Method Parameter
|Name=relatedTarget
|Data type=any
|Description=A reference to the related element.
|Optional=No
}}{{Method Parameter
|Name=offsetX
|Data type=Number
|Description=The x-coordinate of the event in the element.
|Optional=No
}}{{Method Parameter
|Name=offsetY
|Data type=Number
|Description=The y-coordinate of the event in the element.
|Optional=No
}}{{Method Parameter
|Name=width
|Data type=Number
|Description=The contact width of the pointer point specified by pointerId. Default: 0
|Optional=No
}}{{Method Parameter
|Name=height
|Data type=Number
|Description=The contact height of the pointer point specified by pointerId. Default: 0
|Optional=No
}}{{Method Parameter
|Name=pressure
|Data type=Number
|Description=Pen pressure normalized in a range of 0 to 255. Default: 0
|Optional=No
}}{{Method Parameter
|Name=tiltX
|Data type=Number
|Description=The plane angle between the Y-Z plane and the plane containing the transducer axis and the Y axis.  A positive X Tilt is to the right.

This quantity is used in conjunction with Y Tilt to represent the tilt away from normal of a transducer, such as a stylus.

Range: -90 to +90
Default: 0
|Optional=No
}}{{Method Parameter
|Name=tiltY
|Data type=Number
|Description=Represents the angle between the X-Z and transducer-X planes. 

A positive Y Tilt is toward the user.

Range: -90 to +90
Default: 0
|Optional=No
}}{{Method Parameter
|Name=pointerId
|Data type=Number
|Description=Specifies the unique ID of the contact. Default: 0
|Optional=No
}}{{Method Parameter
|Name=pointerType
|Data type=String
|Description=Indicates whether the source is touch, pen or mouse. Default: ""
|Optional=No
}}{{Method Parameter
|Name=isPrimary
|Data type=Boolean
|Description=Indicates whether this is the primary pointer that is used to control the mouse position in a multi-touch scenario. Default: false
|Optional=No
}}
|Method_applies_to=dom/PointerEvent
|Example_object_name=event
|Javascript_data_type=void
|Return_value_description=This method does not return a value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var retval {{=}} PointerEvent.initPointerEvent(typeArg, canBubbleArg, cancelableArg, viewArg, detailArg, screenXArg, screenYArg, clientXArg, clientYArg, ctrlKeyArg, altKeyArg, shiftKeyArg, metaKeyArg, buttonArg, relatedTargetArg, offsetXArg, offsetYArg, widthArg, heightArg, pressure, rotation, tiltX, tiltY, pointerIdArg, pointerType, hwTimestampArg, isPrimary); 
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Pointer Events
|URL=http://www.w3.org/TR/pointerevents
|Status=Working Draft
|Relevant_changes=3.1.3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=IE10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=The PointerEvent object and associated events are supported with the MS prefix. E.g., [http://msdn.microsoft.com/en-us/library/ie/hh772103(v=vs.85).aspx MSPointerEvent]
}}
}}
{{See_Also_Section
|External_links=*[http://www.w3.org/TR/pointerevents/#pointerevent-constructor Pointer Events, Section 3.1.3: PointerEvent Constructor]
*[http://www.w3.org/TR/pointerevents/#examples Pointer Events, Section 9: Dispatching an untrusted pointer event example]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772109(v=vs.85).aspx initPointerEvent Method]
|HTML5Rocks_link=
}}