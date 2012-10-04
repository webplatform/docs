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
{{Method Parameter|Name=keyArg|Data type=BSTR|Description=The [[dom/events/apis/constants/key identifiers|'''key identifier''']]. This value is returned in the [[dom/properties/key|'''key''']]  property of the event.|Optional=}}
{{Method Parameter|Name=locationArg|Data type=unsigned long|Description=The location of the key on the device. This value is returned in the [[dom/properties/location|'''location''']]  property of the event.|Optional=}}
{{Method Parameter|Name=modifiersListArg|Data type=BSTR|Description=A space-separated list of any of the following values:|Optional=}}
{{Method Parameter|Name=repeat|Data type=VARIANT_BOOL|Description=The number of times this key has been pressed. This value is returned in the [[dom/properties/repeat2|'''repeat''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=locale|Data type=BSTR|Description=The locale name. This value is returned in the [[dom/properties/locale|'''locale''']] attribute of the event.|Optional=}}
|Method_applies_to=dom/objects/KeyboardEvent
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
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}