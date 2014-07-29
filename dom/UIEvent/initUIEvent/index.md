{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new user interface event that the  [[dom/Document/createEvent|createEvent]] method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|type]] property.
valid values are:

abort - An onabort event. 
error - An onerror event. 
load - An onload event. 
select - An onselect event. 
resize - An onresize event. 

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
|Name=view
|Data type=DOM Node
|Description=The window on which this event is occurring.  Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/UIEvent/detail|detail]]  property  of the event.
|Optional=No
}}
|Method_applies_to=dom/UIEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var evt {{=}} document.createEvent("UIEvents");
// creates a click event that bubbles, can be cancelled,
// and with its view and detail property initialized to window and 1,
// respectively
evt.initUIEvent("click", true, true, window, 1);
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.1
}}
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/event.initUIEvent event.initUIEvent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975256(v=vs.85).aspx initUIEvent Method]
|HTML5Rocks_link=
}}