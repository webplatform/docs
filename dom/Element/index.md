{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/Node
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''Element''' interface represents an element in an HTML or XML document. Elements may have attributes associated with them; since the '''Element''' interface inherits from [[dom/Node|'''Node''']], the generic '''Node''' interface attribute '''attributes''' may be used to retrieve the set of all attributes for an element. There are methods on the '''Element''' interface to retrieve either an [[dom/attributes|'''attribute''']] object by name or an attribute value by name. In XML, where an attribute value may contain entity references, an '''attribute''' object should be retrieved to examine the possibly fairly complex sub-tree representing the attribute value. On the other hand, in HTML, where all attributes have simple string values, methods to directly access an attribute value can safely be used as a convenience.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_htmlref\ie]:%20Element object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
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
|Specifications=
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