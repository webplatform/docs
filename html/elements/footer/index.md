{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
|High-level issues=Needs Flags, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''footer''' element (&lt;footer&gt;) represents content of the end of the nearest ancestor sectioning content or sectioning root element.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=The basic motivation for introducing the footer element in HTML5 was to eliminate the overuse of [[html/elements/div|&lt;div&gt;]] elements and creating a suitable element for the links and text that are usually located at the bottom of the webpages.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example defines two footers, one at the top and one at the bottom, with the same content.
|Code=&lt;body&gt;
 &lt;!-- First footer --&gt;
 &lt;footer&gt;&lt;a href{{=}}"../"&gt;Back to index...&lt;/a&gt;&lt;/footer&gt;
 &lt;h1&gt;Lorem ipsum&lt;/h1&gt;
 &lt;p&gt;Insert long article here.&lt;/p&gt;
 &lt;!-- Second footer --&gt;
 &lt;footer&gt;&lt;a href{{=}}"../"&gt;Back to index...&lt;/a&gt;&lt;/footer&gt;
&lt;/body&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Footers don't necessarily have to appear at the end of a section, though they usually do. The '''footer''' element can contain entire sections to represent appendices, indexes, license agreements, and similar content. Footers might also contain '''nav''' elements or contact information for the author or editor inside an '''address''' element. When the nearest ancestor element is the '''body''' element, then the footer applies to the whole document.
The '''footer''' element is not sectioning content; it does not introduce a new section.
Windows Internet Explorer 9.  The '''footer''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/sections.html#the-footer-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/sections.html#the-footer-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure, HTML
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>article</code>
*<code>aside</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>header</code>
*<code>hgroup</code>
*<code>mark</code>
*<code>nav</code>
*<code>section</code>
}}
{{Topics|Design, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, Facebook HTML5 Resource Center
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