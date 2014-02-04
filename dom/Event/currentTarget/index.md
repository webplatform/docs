{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the event target that is currently being processed.}}
{{API_Object_Property
|Property_applies_to=dom/Event
|Read_only=Yes
|Example_object_name=event
|Return_value_name=currentTargetElement
|Javascript_data_type=DOM Node
|Return_value_description=The current target of the event.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this property to get the element for which the current event handler is being processed, during the capturing and bubbling phases.
|Notes=The [[dom/Event/target|'''target''']] property returns the element that originally received an event. At event phase <code>AT_TARGET</code>, the '''currentTarget''' and '''target''' objects are the same object.
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
*<code>[[dom/Event/eventPhase|eventPhase]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}