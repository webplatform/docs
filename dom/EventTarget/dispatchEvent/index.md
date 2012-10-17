{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=event
|Data type=Event
|Description=The event object to dispatch.
|Optional=No
}}
|Method_applies_to=apis/EventTarget
|Example_object_name=eventTarget
|Return_value_name=defaultPrevented
|Javascript_data_type=Boolean
|Return_value_description=A '''Boolean''' value that indicates whether any of the event handlers called [[dom/methods/preventDefault|'''preventDefault''']].

Default. The default action is permitted.

The caller should prevent the default action.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Events that the  '''dispatchEvent'''  method dispatches are subject to the same capturing and bubbling behavior as events that  the browser dispatches.
You cannot cancel some events. For more information, see the documentation for the event.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Events
|URL=http://www.w3.org/TR/DOM-Level-2-Events/
|Status=Recommendation
|Relevant_changes=1.3.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*[[dom/document]]
*[[dom/TextNode]]
*[[dom/window]]
*[[apis/xhr/objects/XMLHttpRequest]]
*[[dom/methods/addEventListener]]
*[[canvas/methods/createEvent]]
*[[dom/methods/initEvent]]
}}
{{Topics|DOMEvents, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}