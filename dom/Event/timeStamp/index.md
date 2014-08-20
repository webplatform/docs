{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the time, in milliseconds, when an event occurred.}}
{{API_Object_Property
|Property_applies_to=dom/Event
|Read_only=Yes
|Example_object_name=event
|Return_value_name=eventTimestamp
|Javascript_data_type=Number
|Return_value_description=The event time stamp, in milliseconds since 1970-1-1 00:00:00 UTC.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following event handler displays the event time by using the current locale settings.
|Code=function eventHandler(evt) {
    var dt {{=}} new Date(evt.timeStamp);
    alert(dt.toLocaleString());
}
window.onload {{=}} eventHandler;
}}
}}
{{Notes_Section}}
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
*<code>[[dom/DragEvent|DragEvent]]</code>
*<code>[[dom/Event|Event]]</code>
*<code>[[dom/FocusEvent|FocusEvent]]</code>
*<code>[[dom/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/MessageEvent|MessageEvent]]</code>
*<code>[[dom/MouseEvent|MouseEvent]]</code>
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