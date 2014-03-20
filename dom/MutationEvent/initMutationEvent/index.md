{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Initializes a new DOM mutation (modification) event that the [[dom/Document/createEvent|'''createEvent''']] method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|'''type''']] property.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/Event/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/properties/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=relatedNode
|Data type=DOM Node
|Description=A secondary node that is related to the event. Sets the value for the [[dom/MutationEvent/relatedNode|'''relatedNode''']] property.
|Optional=No
}}{{Method Parameter
|Name=prevValue
|Data type=String
|Description=The previous value of the attribute or text node. Sets the value for the [[dom/MutationEvent/prevValue|'''prevValue''']] property.
|Optional=No
}}{{Method Parameter
|Name=newValue
|Data type=String
|Description=The new value of the attribute or text node. Sets the value for the [[dom/MutationEvent/newValue|'''newValue''']] property.
|Optional=No
}}{{Method Parameter
|Name=attrName
|Data type=String
|Description=The name of the changed attribute in a '''DOMAttrModified''' event. Sets the value for the [[dom/MutationEvent/attrName|'''attrName''']] property.
|Optional=No
}}{{Method Parameter
|Name=attrChange
|Data type=String
|Description=The type of modification in a '''DOMAttrModified''' event. Sets the value for the [[dom/MutationEvent/attrChange|'''attrChange''']] property.
|Optional=No
}}
|Method_applies_to=dom/MutationEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Events
|URL=http://www.w3.org/TR/DOM-Level-2-Events/
|Status=Recommendation
|Relevant_changes=Section 1.6.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=The '''DOMNodeInsertedIntoDocument''' and '''DOMNodeRemovedFromDocument''' '''eventType''' values are not supported.
}}
}}
{{See_Also_Section
|Topic_clusters=Deprecated
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}