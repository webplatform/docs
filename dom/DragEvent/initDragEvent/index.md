{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=eventType|Data type=BSTR|Description=One of the following, or a user-defined custom event type.|Optional=}}
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
{{Method Parameter|Name=detailArg|Data type=Integer|Description='''Integer''' that specifies additional information. This value is returned in the [[dom/properties/detail|'''detail''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=screenXArg|Data type=Integer|Description='''Integer''' that specifies the x-coordinate of the mouse pointer relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenX|'''screenX''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=screenYArg|Data type=Integer|Description='''Integer''' that specifies the y-coordinate of the mouse pointer relative to the upper-left corner of the screen. This value is returned in the [[dom/properties/screenY|'''screenY''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=clientXArg|Data type=Integer|Description='''Integer''' that specifies the x-coordinate of the mouse pointer relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientX|'''clientX''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=clientYArg|Data type=Integer|Description='''Integer''' that specifies the y-coordinate of the mouse pointer relative to the upper-left corner of the browser's client area. This value is returned in the [[dom/properties/clientY|'''clientY''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=ctrlKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/ctrlKey|'''ctrlKey''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=altKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/altKey|'''altKey''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=shiftKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/shiftKey|'''shiftKey''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=metaKeyArg|Data type=VARIANT_BOOL|Description=The value that is returned in the [[dom/properties/metaKey|'''metaKey''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=buttonArg|Data type=USHORT|Description='''Integer''' that specifies the mouse button that caused the event. This value is returned in the [[dom/properties/button|'''button''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=relatedTargetArg|Data type=IEventTarget|Description='''relatedTarget'''|Optional=}}
{{Method Parameter|Name=dataTransferArg|Data type=IHTMLDataTransfer|Description='''dataTransfer'''|Optional=}}
|Method_applies_to=dom/objects/DragEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|E_INVALIDARG
|One or more arguments are invalid.
|}
 


}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.9.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[canvas/methods/createEvent|createEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}