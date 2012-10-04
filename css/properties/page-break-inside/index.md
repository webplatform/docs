{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. 
Neither force nor forbid a page break inside the object.}}
{{CSS_Property_Value|Data Type=avoid |Description=Forbid a page break inside the object, if possible.}}
{{CSS_Property_Value|Data Type=empty string |Description=Behaves the same as '''auto'''.}}
{{CSS_Property_Value|Data Type=inherit |Description=Inherit the value of the same property for the object's parent.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following style rule causes Internet Explorer
to avoid breaking paragraphs across pages.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
@media print {
    p {
        page-break-inside: avoid;
    }
}
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
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
|Import_Notes=
===Syntax===
<code>'''page-break-inside: '''avoid '''{{!}}''' auto '''{{!}}''' inherit '''{{!}}''' empty string</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS How-to - Optimize Pages for Printing Using CSS</code>
|Topic_clusters=Paged Media
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}