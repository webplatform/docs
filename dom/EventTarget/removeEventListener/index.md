{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Removes an event handler that the [[dom/methods/addEventListener|addEventListener]] method registered.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=type
|Data type=String
|Description=The event [[dom/properties/type (event)|'''type''']] that the event handler is registered for.
|Optional=No
}}{{Method Parameter
|Name=listener
|Data type=function
|Description=The event handler function to remove.
|Optional=No
}}{{Method Parameter
|Name=useCapture
|Data type=Boolean
|Description=A '''Boolean''' value that specifies the event phase to remove the event handler from.
|Optional=No
}}
|Method_applies_to=dom/EventTarget
|Example_object_name=target
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=If you register multiple identical event handlers for the same event type, the duplicate event handlers are discarded. You can remove only the first instance.
If the arguments for '''removeEventListener'''  do not identify a  registered event handler, the call to  '''removeEventListener''' has no effect.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 4.3
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*[[dom/Document]]
*[[dom/TextNode]]
*[[dom/Window|Window]]
*[[apis/xhr/objects/XMLHttpRequest]]
*[[dom/methods/addEventListener|addEventListener]]
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}