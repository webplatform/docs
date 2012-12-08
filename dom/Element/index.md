{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents an node of type element in the DOM.}}
{{API_Object
|Subclass_of=dom/Node
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Elements may have attributes associated with them; use the [[dom/properties/attributes|attributes]] property to retrieve the set of all attributes for an element. There are methods on this object to retrieve either an [[dom/attributes|'''attribute''']] object by name ([[dom/methods/getAttributeNode|getAttributeNode]]) or an attribute value by name ([[dom/methods/getAttribute|getAttribute]]).
In XML, where an attribute value may contain entity references, an '''attribute''' object should be retrieved to examine the possibly fairly complex sub-tree representing the attribute value. On the other hand, in HTML, where all attributes have simple string values, methods to directly access an attribute value can safely be used as a convenience.
|Import_Notes====Additional Members (MSDN)===
The '''Element''' object has these types of members:
[[#Additional_Events|Additional Events]]
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Events====
The '''Element''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/mspointercancel|'''onmspointercancel''']]
{{!}}Fires when the system cancels a pointer event.
{{!}}}
 

====Additional Methods====
The '''Element''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[css/regions/MSRange-collection/apis/methods/ms-get-region-content|'''msGetRegionContent''']]
{{!}}Returns an array of Range instances corresponding to the content from the region flow that is positioned in the region.
{{!}}}
 

====Additional Properties====
The '''Element''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[css/properties/ms-content-zoom-factor|'''msContentZoomFactor''']]
{{!}}Gets or sets a value that indicates the content zoom factor.
{{!}}-
{{!}}[[css/regions/MSRange-collection/apis/properties/ms-region-overflow|'''msRegionOverflow''']]
{{!}}Determines if content fully fits into the region or not.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
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