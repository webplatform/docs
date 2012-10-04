{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=eventType|Data type=BSTR|Description=One of the following values, or a user-defined custom event type:|Optional=}}
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
{{Method Parameter|Name=data|Data type=BSTR|Description=The cross-document message. This value is returned as the [[dom/properties/data|'''data''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=origin|Data type=BSTR|Description=The originating domain of the message. This value is returned as the [[dom/properties/origin|'''origin''']] attribute of the event.|Optional=}}
{{Method Parameter|Name=lastEventId|Data type=BSTR|Description=Not used. Set  this parameter to  an empty string.|Optional=}}
{{Method Parameter|Name=source|Data type=IHTMLWindow2|Description=A reference to the '''window''' that generated the event. This value is returned as the [[dom/properties/source|'''source''']] attribute of the event.|Optional=}}
|Method_applies_to=dom/objects/MessageEvent
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
|Notes=
===Remarks===
The ''lastEventId'' parameter emulates server-initiated messages, which Windows Internet Explorer 9 does not support.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 6.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/MessageEvent|MessageEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}