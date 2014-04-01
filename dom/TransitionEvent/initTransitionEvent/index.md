{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=typeArg
|Data type=any
|Description=Specifies the event type.
|Optional=No
}}{{Method Parameter
|Name=canBubbleArg
|Data type=any
|Description=Specifies whether or not the event can bubble.
|Optional=No
}}{{Method Parameter
|Name=cancelableArg
|Data type=any
|Description=Specifies whether or not the event's default action can be prevented. Since a '''TransitionEvent''' is purely for notification, there is no default action.
|Optional=No
}}{{Method Parameter
|Name=propertyNameArg
|Data type=any
|Description=Specifies the name of the property associated with the [[dom/Event|'''Event''']].
|Optional=No
}}{{Method Parameter
|Name=elapsedTimeArg
|Data type=any
|Description=Specifies the amount of time, in seconds, the transition has been running at the time of initialization.
|Optional=No
}}
|Method_applies_to=dom/TransitionEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK

}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This method is used to initialize the value of a '''TransitionEvent'''. This method may only be called before the '''TransitionEvent''' has been dispatched via the [[dom/EventTarget/dispatchEvent|'''dispatchEvent''']] method, though it may be called multiple times during that phase if necessary. If called multiple times, the final invocation takes precedence.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
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