{{Page_Title}}
{{Flags
|Editorial notes=Needs examples and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Initializes a new drag event.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|'''type''']] property.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/Event/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=cancelable
|Data type=String
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/Event/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Index=3
|Name=view
|Data type=DOM Node
|Description=The window on which this event is occurring.  Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Index=4
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/UIEvent/detail|'''detail''']] property  of the event.
|Optional=No
}}{{Method Parameter
|Index=5
|Name=screenX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. This value is returned in the [[dom/MouseEvent/screenX|'''screenX''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=6
|Name=screenY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. This value is returned in the [[dom/MouseEvent/screenY|'''screenY''']] property of the event.
|Optional=No
}}{{Method Parameter
|Name=clientX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. This value is returned in the [[dom/MouseEvent/clientX|'''clientX''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=7
|Name=clientY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. This value is returned in the [[dom/MouseEvent/clientY|'''clientY''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=8
|Name=ctrlKey
|Data type=Boolean
|Description=The value that is returned in the [[dom/KeyboardEvent/ctrlKey|'''ctrlKey''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=9
|Name=altKey
|Data type=Boolean
|Description=The value that is returned in the [[dom/KeyboardEvent/altKey|'''altKey''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=10
|Name=shiftKey
|Data type=Boolean
|Description=The value that is returned in the [[dom/KeyboardEvent/shiftKey|'''shiftKey''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=11
|Name=metaKey
|Data type=Boolean
|Description=The value that is returned in the [[dom/KeyboardEvent/metaKey|'''metaKey''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=12
|Name=button
|Data type=Number
|Description=The mouse button that caused the event. This value is returned in the [[dom/MouseEvent/button|'''button''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=13
|Name=relatedTarget
|Data type=DOM Node
|Description=A secondary element that is involved in the event. This value is returned in the [[dom/MouseEvent/relatedTarget|'''relatedTarget''']] property of the event.
|Optional=No
}}{{Method Parameter
|Index=14
|Name=dataTransfer
|Data type=String
|Description=A [[dom/DataTransfer|DataTransfer]] object.
|Optional=No
}}
|Method_applies_to=dom/DragEvent
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