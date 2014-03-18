{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new cross-document message (XDM) event  that the  [[dom/Document/createEvent|'''createEvent''']] method created.}}
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
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/Event/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=data
|Data type=any
|Description=The cross-document message. Sets the value for the [[dom/MessageEvent/data|'''data''']] property.
|Optional=No
}}{{Method Parameter
|Name=origin
|Data type=String
|Description=The originating domain of the message. Sets the value for the [[dom/MessageEvent/origin|'''origin''']] property.
|Optional=No
}}{{Method Parameter
|Name=lastEventId
|Data type=String
|Description=Not used. Set this parameter to an empty string.
|Optional=No
}}{{Method Parameter
|Name=source
|Data type=Object
|Description=A reference to the '''window''' that generated the event. Sets the value for the [[dom/MessageEvent/source|'''source''']] property.
|Optional=No
}}
|Method_applies_to=dom/MessageEvent
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
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 6.1
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/
|Status=Living Standard
|Relevant_changes=Section 6.1
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
|Note=The ''lastEventId'' parameter emulates server-initiated messages, which are unsupported.
}}
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