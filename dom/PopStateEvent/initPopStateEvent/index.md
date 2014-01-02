{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=typeArg|Data type=DOMString|Description=The type of the event being created.|Optional=}}
{{Method Parameter|Name=canBubbleArg|Data type=boolean|Description=Indicates whether the event can bubble.
When true,
the event propagates upward. 
When false,
the event does not propagate upward.|Optional=}}
{{Method Parameter|Name=cancelableArg|Data type=Boolean|Description=Indicates whether the event’s default action can be prevented.
When true, the default action can be canceled. 
When false, the default action cannot be canceled.|Optional=}}
{{Method Parameter|Name=stateArg|Data type=any|Description=The object to be applied to the [[dom/properties/state|'''state''']] property.|Optional=}}
|Method_applies_to=dom/PopStateEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK

Type: '''HRESULT'''

This method can return one of these values.

S_OK


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Initializes attributes of an event created through the [[dom/methods/createEventObject|'''createEvent''']] method. This method can only be called before the event has been dispatched via the [[dom/methods/dispatchEvent|'''dispatchEvent''']] method. If the method is called several times before invoking '''dispatchEvent''', only the final invocation takes precedence. This method has no effect if called after the event has been dispatched.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/PopStateEvent|PopStateEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}