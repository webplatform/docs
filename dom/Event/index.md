{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Represents an event.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=You can access the attributes of the '''Event''' object from all event types.
|Import_Notes====Additional Members (MSDN)===
The '''Event''' object has these types of members:
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Methods====
The '''Event''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/initEvent|'''initEvent''']]
{{!}}Initializes a new generic event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
{{!}}-
{{!}}[[dom/methods/preventDefault|'''preventDefault''']]
{{!}}Cancels the default action of an event.
{{!}}-
{{!}}[[dom/methods/stopImmediatePropagation|'''stopImmediatePropagation''']]
{{!}}Prevents any further propagation of an event.
{{!}}-
{{!}}[[dom/methods/stopPropagation|'''stopPropagation''']]
{{!}}Prevents propagation of an event beyond the current target.
{{!}}}
 

====Additional Properties====
The '''Event''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/currentTarget|'''currentTarget''']]
{{!}}Gets the event target that is currently being processed.
{{!}}-
{{!}}[[dom/properties/defaultPrevented|'''defaultPrevented''']]
{{!}}Gets a value that indicates whether the default action should be canceled.
{{!}}-
{{!}}[[dom/properties/eventPhase|'''eventPhase''']]
{{!}}Gets the event phase that is being evaluated.
{{!}}-
{{!}}[[dom/properties/target|'''target''']]
{{!}}Gets the element that is the target of the event.
{{!}}-
{{!}}[[dom/properties/timeStamp|'''timeStamp''']]
{{!}}Gets the time, in milliseconds, when an event occurred.
{{!}}}
 
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
*<code>[[dom/objects/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/objects/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/objects/CustomEvent|CustomEvent]]</code>
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
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}