{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the element for the specified x coordinate and the specified y coordinate.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=A number that specifies the X-offset, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=A number that specifies the Y-offset, in pixels.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=The element at the given point.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Listen for click event on entire document, log nodeName of element found with elementFromPoint()
|Code=document.addEventListener("click", function(event){
  var el = document.elementFromPoint(event.clientX, event.clientY);
  console.log(el.nodeName);
});
}}
}}
{{Notes_Section
|Usage=This methods is used to get the element from the document whose elementFromPoint method is being called which is the ''topmost element'' which lies under the given point.  To get an element, specify the point via coordinates, in CSS pixels, relative to the upper-left-most point in the window or frame containing the document.
|Notes=Coordinates are supplied in client coordinates. The upper-left corner of the client area is (0,0). For '''elementFromPoint''' to exhibit expected behavior, the object or element located at position (x, y) must support and respond to mouse events.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSSOM View Module
|URL=http://dev.w3.org/csswg/cssom-view/#widl-Document-elementFromPoint-Element-float-x-float-y
|Status=Editor's Draft 3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.53
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/MouseEvent/clientX|clientX]]</code>
*<code>[[dom/MouseEvent/clientY|clientY]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/document.elementFromPoint
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}