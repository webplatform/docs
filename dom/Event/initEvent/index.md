{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes a new generic event that the  [[dom/methods/createEvent|'''createEvent''']] method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the [[dom/properties/type (event)|'''type''']] property.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/properties/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/methods/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/properties/cancelable|cancelable]] property.
|Optional=No
}}
|Method_applies_to=dom/objects/Event
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
|Notes=You can call the '''initEvent'''  method only before the   [[dom/methods/dispatchEvent|'''dispatchEvent''']] method dispatches the event object. After the event is dispatched, its properties cannot be changed.
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
*<code>[[dom/objects/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/objects/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/objects/CustomEvent|CustomEvent]]</code>
*<code>[[dom/objects/Event|Event]]</code>
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/FocusEvent|FocusEvent]]</code>
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/objects/MessageEvent|MessageEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/MutationEvent|MutationEvent]]</code>
*<code>[[dom/objects/MSSiteModeEvent|MSSiteModeEvent]]</code>
*<code>[[dom/objects/StorageEvent|StorageEvent]]</code>
*<code>[[dom/objects/TextEvent|TextEvent]]</code>
*<code>[[dom/objects/UIEvent|UIEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/bubbles|bubbles]]</code>
*<code>[[dom/properties/cancelable|cancelable]]</code>
*<code>[[dom/methods/dispatchEvent|dispatchEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}