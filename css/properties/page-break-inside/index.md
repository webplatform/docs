{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the page-breaking behavior inside an element.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. 
Neither force nor forbid a page break inside the object.
}}{{CSS Property Value
|Data Type=avoid
|Description=Forbid a page break inside the object, if possible.
}}{{CSS Property Value
|Data Type=empty string
|Description=Behaves the same as '''auto'''.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherit the value of the same property for the object's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule causes Internet Explorer
to avoid breaking paragraphs across pages.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
@media print {
    p {
        page-break-inside: avoid;
    }
}
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This property applies when the document is printed.
Normally, Windows Internet Explorer attempts to avoid page breaks
inside tables, blocks with borders, and positioned or floated elements.
The '''page-break-inside''' attribute extends this behavior to other elements. A value of '''avoid''' instructs the browser to start the element on the following page if there is not enough room for it on the current page.
Page-break behavior is inherited from parent objects. A potential
page-break location is also influenced by the
[[css/properties/page-break-after|'''page-break-after''']]
attribute of the preceding object, and/or the
[[css/properties/page-break-before|'''page-break-before''']]
attribute of the following object.
This property requires Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''page-break-inside: '''avoid '''{{!}}''' auto '''{{!}}''' inherit '''{{!}}''' empty string</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fragmentation Module Level 3, 3.3. Page Break Aliases: the ‘page-break-before’, ‘page-break-after’, and ‘page-break-inside’ properties
|URL=http://www.w3.org/TR/css3-break/#page-break
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS Paged Media Module Level 3, 9. Page Breaks
|URL=http://www.w3.org/TR/css3-page/#page-breaks
|Status=W3C Working Draft
|Relevant_changes=The CSS Fragmentation Module module defines CSS box fragmentation, including across page breaks.
}}{{Related Specification
|Name=CSS Level 2 (Revision 1), 13.3.1 Page break properties: 'page-break-before', 'page-break-after', 'page-break-inside'
|URL=http://www.w3.org/TR/CSS2/page.html#page-break-props
|Status=W3C Recommendation
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=19
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.3
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Paged Media
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS How-to - Optimize Pages for Printing Using CSS</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}