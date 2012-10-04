{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=typeArg|Data type=DOMString|Description=Specifies the event type.|Optional=}}
{{Method Parameter|Name=canBubbleArg|Data type=boolean|Description=Specifies whether or not the event can bubble.|Optional=}}
{{Method Parameter|Name=cancelableArg|Data type=boolean|Description=Specifies whether or not the event's default action can be prevented. Since a '''TransitionEvent''' is purely for notification, there is no default action.|Optional=}}
{{Method Parameter|Name=propertyNameArg|Data type=DOMString|Description=Specifies the name of the property associated with the [[dom/objects/Event|'''Event''']].|Optional=}}
{{Method Parameter|Name=elapsedTimeArg|Data type=float|Description=Specifies the amount of time, in seconds, the transition has been running at the time of initialization.|Optional=}}
|Method_applies_to=dom/objects/TransitionEvent
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
This method is used to initialize the value of a '''TransitionEvent'''. This method may only be called before the '''TransitionEvent''' has been dispatched via the [[dom/methods/dispatchEvent|'''dispatchEvent''']] method, though it may be called multiple times during that phase if necessary. If called multiple times, the final invocation takes precedence.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/objects/TransitionEvent|transitionEvent]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}