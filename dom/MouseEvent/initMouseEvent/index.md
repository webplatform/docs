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
{{Method Parameter|Name=viewArg|Data type=IHTMLWindow2|Description='''window'''|Optional=}}
{{Method Parameter|Name=detailArg|Data type=Integer|Description=A number that can provide additional information about the event. This value is returned in the [[dom/properties/detail|'''detail''']]  property of the event.|Optional=}}
{{Method Parameter|Name=screenXArg|Data type=Integer|Description=The x-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenX|'''screenX''']]  property of the event.|Optional=}}
{{Method Parameter|Name=screenYArg|Data type=Integer|Description=The y-coordinate of the mouse pointer, relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenY|'''screenY''']]  property of the event.|Optional=}}
{{Method Parameter|Name=clientXArg|Data type=Integer|Description=The x-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientX|'''clientX''']]  property of the event.|Optional=}}
{{Method Parameter|Name=clientYArg|Data type=Integer|Description=The y-coordinate of the mouse pointer, relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientY|'''clientY''']]  property of the event.|Optional=}}
{{Method Parameter|Name=ctrlKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/ctrlKey|'''ctrlKey''']]  property of the event.|Optional=}}
{{Method Parameter|Name=altKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/altKey|'''altKey''']]  property of the event.|Optional=}}
{{Method Parameter|Name=shiftKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/shiftKey|'''shiftKey''']]  property of the event.|Optional=}}
{{Method Parameter|Name=metaKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/metaKey|'''metaKey''']]  property of the event.|Optional=}}
{{Method Parameter|Name=buttonArg|Data type=unsigned short|Description=The mouse button that caused the event. This value is returned in the [[dom/properties/button|'''button''']]  property of the event.|Optional=}}
{{Method Parameter|Name=relatedTargetArg|Data type=IEventTarget|Description=A reference to the related element. For more information about how related elements are used with mouse events, see [[dom/properties/relatedTarget|'''relatedTarget''']].|Optional=}}
|Method_applies_to=dom/objects/MouseEvent
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
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>[[dom/methods/initPointerEvent|initPointerEvent]]</code>
*<code>[[dom/methods/initGestureEvent|initGestureEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}