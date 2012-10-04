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
{{Method Parameter|Name=detail|Data type=Integer|Description=An'''Integer'''  value that specifies additional information. This value is returned in the [[dom/properties/detail|'''detail''']]  property  of the event.|Optional=}}
|Method_applies_to=dom/objects/UIEvent
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
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/objects/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/FocusEvent|FocusEvent]]</code>
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/TextEvent|TextEvent]]</code>
*<code>[[dom/objects/UIEvent|UIEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}