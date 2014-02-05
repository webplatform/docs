{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new generic event that the  [[dom/Document/createEvent|'''createEvent''']] method created.}}
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
}}
|Method_applies_to=dom/Event
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code example creates a custom event that bubbles but cannot be canceled.
|Code=var evt {{=}} document.createEvent("Event");
evt.initEvent("custom", true, false);
document.getElementById('target').dispatchEvent(evt);
}}
}}
{{Notes_Section
|Usage=Use this method before the   [[dom/EventTarget/dispatchEvent|'''dispatchEvent''']] method dispatches the event object, to set some properties of the event.
|Notes=After the event is dispatched, its properties cannot be changed.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 4.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/CustomEvent|CustomEvent]]</code>
*<code>[[dom/Event|Event]]</code>
*<code>[[dom/DragEvent|DragEvent]]</code>
*<code>[[dom/FocusEvent|FocusEvent]]</code>
*<code>[[dom/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/MessageEvent|MessageEvent]]</code>
*<code>[[dom/MouseEvent|MouseEvent]]</code>
*<code>[[dom/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/MutationEvent|MutationEvent]]</code>
*<code>[[dom/StorageEvent|StorageEvent]]</code>
*<code>[[dom/TextEvent|TextEvent]]</code>
*<code>[[dom/UIEvent|UIEvent]]</code>

}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}