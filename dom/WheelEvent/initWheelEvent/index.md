{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=eventType|Data type=BSTR|Description=One of the following values, or a user-defined custom event type.|Optional=}}
{{Method Parameter|Name=canBubble|Data type=VARIANT_BOOL|Description='''VARIANT_TRUE''' (true)



The event should propagate upward. 


'''VARIANT_FALSE''' (false)



The event does not propagate upward. 

|Optional=}}
{{Method Parameter|Name=cancelable|Data type=VARIANT_BOOL|Description='''VARIANT_TRUE''' (true)



The default action can be canceled. 


'''VARIANT_FALSE''' (false)



The default action cannot be canceled. 

|Optional=}}
{{Method Parameter|Name=view|Data type=IHTMLWindow2|Description='''window'''|Optional=}}
{{Method Parameter|Name=detail|Data type=Integer|Description=A number that can provide additional information about the event. This value is returned in the [[dom/properties/detail|'''detail''']]  property of the event.|Optional=}}
{{Method Parameter|Name=screenXArg|Data type=Integer|Description=The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenX|'''screenX''']]  property of the event.|Optional=}}
{{Method Parameter|Name=screenYArg|Data type=Integer|Description=The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenY|'''screenY''']]  property of the event.|Optional=}}
{{Method Parameter|Name=clientXArg|Data type=Integer|Description=The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientX|'''clientX''']]  property of the event.|Optional=}}
{{Method Parameter|Name=clientYArg|Data type=Integer|Description=The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientY|'''clientY''']]  property of the event.|Optional=}}
{{Method Parameter|Name=buttonArg|Data type=unsigned short|Description=The mouse button that caused the event. This value is returned in the [[dom/properties/button|'''button''']]  property of the event.|Optional=}}
{{Method Parameter|Name=relatedTargetArg|Data type=IEventTarget|Description=A reference to the related element. For more information, see [[dom/properties/relatedTarget|'''relatedTarget''']].|Optional=}}
{{Method Parameter|Name=modifiersListArg|Data type=BSTR|Description=A space-separated list of any of the following values:|Optional=}}
{{Method Parameter|Name=deltaX|Data type=Integer|Description=The distance that the mouse wheel has rotated around the x-axis. This value is returned in the [[dom/properties/deltaX|'''deltaX''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=deltaY|Data type=Integer|Description=The distance that the mouse wheel has rotated around the y-axis. This value is returned in the [[dom/properties/deltaY|'''deltaY''']]  property of the event.|Optional=}}
{{Method Parameter|Name=deltaZ|Data type=Integer|Description=The distance that the mouse wheel has rotated around the z-axis. This value is returned in the [[dom/properties/deltaZ|'''deltaZ''']]  property of the event.|Optional=}}
{{Method Parameter|Name=deltaMode|Data type=unsigned long|Description=The delta mode of the event. This value is returned in the [[dom/properties/deltaMode|'''deltaMode''']]  property of the event.|Optional=}}
|Method_applies_to=dom/objects/WheelEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}