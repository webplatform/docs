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
{{Method Parameter|Name=relatedNodeArg|Data type=IDispatch|Description=A secondary node that is related to the event. This value is returned as the [[dom/properties/relatedNode|'''relatedNode''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=prevValueArg|Data type=BSTR|Description=The previous value of the attribute or text node. This value is returned as the [[dom/properties/prevValue|'''prevValue''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=newValueArg|Data type=BSTR|Description=The new value of the attribute or text node. This value is returned as the [[dom/properties/newValue|'''newValue''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=attrNameArg|Data type=BSTR|Description=The name of the changed attribute in a '''DOMAttrModified''' event. This value is returned as the [[dom/properties/attrName|'''attrName''']]  property  of the event.|Optional=}}
{{Method Parameter|Name=attrChangeArg|Data type=unsigned short|Description=The type of modification in a '''DOMAttrModified''' event. This value is returned as the [[dom/properties/attrChange|'''attrChange''']]  property  of the event.|Optional=}}
|Method_applies_to=dom/objects/MutationEvent
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
The '''DOMNodeInsertedIntoDocument''' and '''DOMNodeRemovedFromDocument''' event type values are not supported.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.8


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/MutationEvent|MutationEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}