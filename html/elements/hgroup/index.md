{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|(Obsolete) The '''hgroup''' element (&lt;hgroup&gt;) is typically used to group a set of one or more h1-h6 elements — to group, for example, a section title and an accompanying subtitle. The '''hgroup''' element (&lt;hgroup&gt;) element is obsolete in HTML5.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=
==Obsolete==
The hgroup element is obsolete in HTML. Consider the [[html/elements/header|header]] element, or a <code>&lt;span class="subheading"&gt;</code> element with differentiated styling.

== Point ==
*The element is used to group a set of h1–h6 elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines. [[#Example_A|[Example A]]]
*For the purposes of document summaries, outlines, and the like, the text of hgroup elements is defined to be the text of the highest ranked h1–h6 element descendant of the hgroup element, if there are any such elements, and the first such element if there are multiple elements with that rank.
*The rank of an hgroup element is the rank of the highest-ranked h1–h6 element descendant of the hgroup element, if there are any such elements, or otherwise the same as for an h1 element (the highest rank).

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following is an example of a valid heading. The '''hgroup''' masks the '''h2''' element (which acts as a secondary title) from the outline algorithm.
|Code=&lt;hgroup&gt;
 &lt;h1&gt;Dr. Strangelove&lt;/h1&gt;
 &lt;h2&gt;Or: How I Learned to Stop Worrying and Love the Bomb&lt;/h2&gt;
&lt;/hgroup&gt;
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=For document summaries and outlines, the text of '''hgroup''' elements is defined as the text of the highest ranked '''h1-h6''' element descendant, or the first such element if there are multiple elements with the highest rank. If there are no such elements, then the text of the '''hgroup''' element is the empty string. The following script demonstrates how to implement this behavior.
|Code=function findHeadings(node)
{
    // First check if this node has an &lt;hgroup&gt;.
    var hg {{=}} node.getElementsByTagName("HGROUP");
    if(hg.length&gt;0)
        node {{=}} hg[0];
    // Now find the highest ranking heading.
    var ranks {{=}} [ "H1","H2","H3","H4","H5","H6" ];
    for (var i{{=}}0; i&lt;ranks.length; i++) {
        var headings {{=}} node.getElementsByTagName(ranks[i]);
        if(headings.length&gt;0)
            return headings[0].textContent;
    }
    // No headings present, return empty string.
    return "";
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Windows Internet Explorer 9.  The '''hgroup''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
The '''hgroup''' element is used to group a set of '''h1-h6''' elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines. Other elements of heading content in the '''hgroup''' element indicate subheadings or subtitles.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=http://www.w3.org/html/wg/drafts/html/CR/obsolete.html#hgroup
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>article</code>
*<code>aside</code>
*<code>figcaption</code>
*<code>figure</code>
*<code>footer</code>
*<code>header</code>
*<code>mark</code>
*<code>nav</code>
*<code>section</code>
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