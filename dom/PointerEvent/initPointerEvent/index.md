{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=typeArg|Data type=DOMString|Description=The type of the event being created|Optional=}}
{{Method Parameter|Name=canBubbleArg|Data type=boolean|Description=Indicates whether the event can bubble.
When true
the event should propagate upward. 
When false
the event does not propagate upward.|Optional=}}
{{Method Parameter|Name=cancelableArg|Data type=boolean|Description=Indicates whether the event’s default action can be prevented.
When true, the default action can be canceled. 
When false, the default action cannot be canceled.|Optional=}}
{{Method Parameter|Name=viewArg|Data type=AbstractView|Description=The view in which the event is taking place.|Optional=}}
{{Method Parameter|Name=detailArg|Data type=Integer|Description=Specifies some detailed information depending upon the event.|Optional=}}
{{Method Parameter|Name=screenXArg|Data type=Integer|Description=The x-coordinate of the event in screen coordinates relative to the upper left corner of the screen.|Optional=}}
{{Method Parameter|Name=screenYArg|Data type=Integer|Description=The y-coordinate of the event in screen coordinates relative to the upper left corner of the screen.|Optional=}}
{{Method Parameter|Name=clientXArg|Data type=float|Description=The x-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.|Optional=}}
{{Method Parameter|Name=clientYArg|Data type=float|Description=The y-coordinate of the event in client coordinates relative to the upper-left corner of the document's client area.|Optional=}}
{{Method Parameter|Name=ctrlKeyArg|Data type=boolean|Description=Indicates the state of the Ctrl key.
When true, the left or right Ctrl key is pressed. 
If false, neither Ctrl key is pressed.|Optional=}}
{{Method Parameter|Name=altKeyArg|Data type=boolean|Description=Indicates the state of the Alt key.
When true, the left or right Alt key is pressed. 
If false, neither Alt key is pressed.|Optional=}}
{{Method Parameter|Name=shiftKeyArg|Data type=boolean|Description=Indicates the state of the Shift key.
When true, the left or right Shift key is pressed. 
If false, neither Shift key is pressed.|Optional=}}
{{Method Parameter|Name=metaKeyArg|Data type=boolean|Description=Indicates the state of the Meta/Command key.
If true, the left or right Meta/Command key is pressed. 
If false
neither Meta/Command key is pressed.|Optional=}}
{{Method Parameter|Name=buttonArg|Data type=unsigned short|Description=If the event is caused by a mouse event, this indicates the mouse button that caused the event.|Optional=}}
{{Method Parameter|Name=relatedTargetArg|Data type=EventTarget|Description=A reference to the related element.|Optional=}}
{{Method Parameter|Name=offsetXArg|Data type=float|Description=The x-coordinate of the event in the element.|Optional=}}
{{Method Parameter|Name=offsetYArg|Data type=float|Description=The y-coordinate of the event in the element.|Optional=}}
{{Method Parameter|Name=widthArg|Data type=Integer|Description=The contact width of the pointer point specified by pointerId.|Optional=}}
{{Method Parameter|Name=heightArg|Data type=Integer|Description=The contact height of the pointer point specified by pointerId.|Optional=}}
{{Method Parameter|Name=pressure|Data type=float|Description=Pen pressure normalized in a range of 0 to 255.|Optional=}}
{{Method Parameter|Name=rotation|Data type=Integer|Description=Clockwise rotation of the cursor around its own major axis. 
Range: 0 to 359.|Optional=}}
{{Method Parameter|Name=tiltX|Data type=Integer|Description=The plane angle between the Y-Z plane and the plane containing the transducer axis and the Y axis.  A positive X Tilt is to the right.

This quantity is used in conjunction with Y Tilt to represent the tilt away from normal of a transducer, such as a stylus.

Range: -90 to +90.|Optional=}}
{{Method Parameter|Name=tiltY|Data type=Integer|Description=Represents the angle between the X-Z and transducer-X planes. 

A positive Y Tilt is toward the user.

Range: -90 to +90.|Optional=}}
{{Method Parameter|Name=pointerIdArg|Data type=Integer|Description=Specifies the unique ID of the contact.|Optional=}}
{{Method Parameter|Name=pointerType|Data type=Integer|Description=Indicates whether the source is touch,  pen or mouse.|Optional=}}
{{Method Parameter|Name=hwTimestampArg|Data type=unsigned long long|Description=Used to specify the time at which the event was created in microseconds.|Optional=}}
{{Method Parameter|Name=isPrimary|Data type=boolean|Description=Indicates whether this is the primary pointer that is used to control the mouse position in a multi-touch scenario.|Optional=}}
|Method_applies_to=dom/objects/MSPointerEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.

This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/MSPointerEvent|MSPointerEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}