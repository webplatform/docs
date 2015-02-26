{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Examples need "try it" link.
Add Category, Parent, Children and Compatibility information.
Write something for main content.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''figcaption''' (&lt;figcaption&gt;) defines a caption or legend for a figure element.
This element is new in HTML5.
}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=As the first child of a figure element
|Code=<nowiki>
<figure>
  <figcaption>The Stata Center</figcaption>
  <img src="stata.jpg" alt="The Stata Center Building"/>
</figure>
</nowiki>
|LiveURL=
}}{{Single Example
|Language=
|Description=
|Code=<nowiki>
<figure>
  <img src="stata.jpg" alt="The Stata Center Building">
  <figcaption>The Stata Center</figcaption>
</figure>
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The first '''figcaption''' element child of the '''figure''' element represents the caption of the '''figure''' element's contents. The '''figcaption''' element is rendered in place; to move the caption, place it as the first or the last child of the '''figure''' element.
'''Note'''  If the '''figcaption''' content provides an adequate text alternative for the visual content in the image, the caption can be used as a text alternative for images in lieu of the [[html/attributes/alt|'''alt''']] attribute.
Windows Internet Explorer 9.  The '''figcaption''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-figcaption-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-figcaption-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}