{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a DOM event of the specified type.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=One of the following values. Case is not important.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=event
|Javascript_data_type=DOM Node
|Return_value_description=The created event.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example demonstrates how to create and dispatch a custom event that bubbles and cannot be canceled.
|Code=var evt {{=}} document.createEvent("Event");
evt.initEvent("custom", true, false);
document.getElementById('target').dispatchEvent(evt);
}}{{Single Example
|Language=JavaScript
|Description=To respond to the custom event created previously, the following example adds an event handler that interacts with the event by setting a expando property named <code>detail</code>.
|Code=function reportEvent(evt) {
    evt.detail {{=}} "Success.";
}
var p {{=}} document.getElementById('target');
p.addEventListener("custom", reportEvent, false);
}}
}}
{{Notes_Section
|Notes=If the event object is to be dispatched with [[dom/EventTarget/dispatchEvent|'''dispatchEvent''']], the appropriate event initialization method must be called. For example, after creating an event of type '''UIEvent''', call [[dom/UIEvent/initUIEvent|'''initUIEvent''']] to initialize the event object's values.
'''Security Warning:  '''For security reasons, events generated with '''createEvent''' are untrusted and have a [[dom/Event/isTrusted|'''isTrusted''']] value of  false.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 4.5
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}