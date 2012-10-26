{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=One of the following, or a user-defined custom event type.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event should propagate upward.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=String
|Description=Whether the default action can be canceled.
|Optional=No
}}{{Method Parameter
|Name=viewArg
|Data type=DOM Node
|Description=A '''window''' object.
|Optional=No
}}{{Method Parameter
|Name=detailArg
|Data type=Number
|Description=Additional information. This value is returned in the [[dom/properties/detail|'''detail''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=screenXArg
|Data type=Number
|Description=The x-coordinate of the mouse pointer relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenX|'''screenX''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=screenYArg
|Data type=Number
|Description=The y-coordinate of the mouse pointer relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenY|'''screenY''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=clientXArg
|Data type=String
|Description=The x-coordinate of the mouse pointer relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientX|'''clientX''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=clientYArg
|Data type=Number
|Description=The y-coordinate of the mouse pointer relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientY|'''clientY''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=ctrlKeyArg
|Data type=Boolean
|Description=The value that is returned in the [[dom/properties/ctrlKey|'''ctrlKey''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=altKeyArg
|Data type=Boolean
|Description=The value that is returned in the [[dom/properties/altKey|'''altKey''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=shiftKeyArg
|Data type=Boolean
|Description=The value that is returned in the [[dom/properties/shiftKey|'''shiftKey''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=metaKeyArg
|Data type=Boolean
|Description=The value that is returned in the [[dom/properties/metaKey|'''metaKey''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=buttonArg
|Data type=Number
|Description=The mouse button that caused the event. This value is returned in the [[dom/properties/button|'''button''']] attribute of the event.
|Optional=No
}}{{Method Parameter
|Name=relatedTargetArg
|Data type=DOM Node
|Description='''relatedTarget'''
|Optional=No
}}{{Method Parameter
|Name=dataTransferArg
|Data type=String
|Description='''dataTransfer'''
|Optional=No
}}
|Method_applies_to=dom/objects/DragEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 7.9.2
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/methods/createEvent|createEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}