{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Write main content.
Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''figure''' element (&lt;figure&gt;) represents self-contained content (such as an image), optionally with a caption, that can be referenced as a single unit from the main content of the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=A figure can be given a caption with the [[html/elements/figcaption|figcaption]] element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example shows the '''figure''' element to mark up a code listing. The '''figcaption''' element represents the caption of the figure. The author has also provided a link to the figure in the main content by using a named anchor.
|Code=&lt;!-- Main Content --&gt;
&lt;p&gt;In &lt;a href{{=}}"#l4"&gt;listing 4&lt;/a&gt; we see the primary core interface API declaration.&lt;/p&gt;
&lt;!-- Figure Content --&gt;
&lt;figure id{{=}}"l4"&gt;
    &lt;figcaption&gt;Listing 4. The primary core interface API declaration.&lt;/figcaption&gt;
    &lt;pre&gt;&lt;code&gt;interface PrimaryCore {
 boolean verifyDataLine();
 void sendData(in sequence&amp;lt;byte&gt; data);
 void initSelfDestruct();
}&lt;/code&gt;&lt;/pre&gt;
&lt;/figure&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''figure''' element can be used to annotate content that can be referenced from the main content of the document, such as illustrations, diagrams, photos, code listings, and so on. Figures can be moved away from primary content without affecting the flow of the document.
You can jump to the figure from the main content by using a named anchor. The [[html/attributes/id|'''id''']] attribute of the '''figure''' element specifies the fragment identifier (name of the anchor).
The default CSS for the '''figure''' element is as follows.
 <code>margin: 1em 40px</code>
The '''figure''' element, like '''aside''', separates content from the main flow. Use the '''aside''' element when the content is simply related, but not essential. Use '''figure''' if the content is essential, but position is not important.
Windows Internet Explorer 9.  The '''figure''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-figure-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-figure-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=* [[html/elements/figcaption|figcaption]]
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