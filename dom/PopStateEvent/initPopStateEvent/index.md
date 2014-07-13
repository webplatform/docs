{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Initializes the properties of a PopStateEvent.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=typeArg
|Data type=any
|Description=The type of the event being created.
|Optional=No
}}{{Method Parameter
|Name=canBubbleArg
|Data type=any
|Description=Indicates whether the event can bubble.
When true,
the event propagates upward. 
When false,
the event does not propagate upward.
|Optional=No
}}{{Method Parameter
|Name=cancelableArg
|Data type=Boolean
|Description=Indicates whether the event’s default action can be prevented.
When true, the default action can be canceled. 
When false, the default action cannot be canceled.
|Optional=No
}}{{Method Parameter
|Name=stateArg
|Data type=any
|Description=The object to be applied to the [[dom/PopStateEvent/state|'''state''']] property.
|Optional=No
}}
|Method_applies_to=dom/PopStateEvent
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var evt {{=}} document.createEvent("PopStateEvent");
evt.initPopStateEvent("popstate", false, false, { .. state object  ..});
window.dispatchEvent(evt);
}}
}}
{{Notes_Section
|Notes====Remarks===
Initializes attributes of an event created through the [[dom/Document/createEvent|'''createEvent''']] method. This method can only be called before the event has been dispatched via the [[dom/EventTarget/dispatchEvent|'''dispatchEvent''']] method. If the method is called several times before invoking '''dispatchEvent''', only the final invocation takes precedence. This method has no effect if called after the event has been dispatched.
|Import_Notes====Syntax===

var retval = PopStateEvent.initPopStateEvent(typeArg, canBubbleArg, cancelableArg, stateArg);
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772350(v=vs.85).aspx initPopStateEvent Method]
|HTML5Rocks_link=
}}