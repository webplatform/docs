{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/Event
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following event handler displays the event time by using the current locale settings.
|LiveURL=
|Code=
function eventHandler(evt) {
    var dt {{=}} new Date(evt.timeStamp);
    alert(dt.toLocaleString());
}
window.onload {{=}} eventHandler; 
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
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
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}