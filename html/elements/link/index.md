{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Discussion on semantics of hyperlinks
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Enables the current document to establish links to external documents.}}
{{Markup_Element
|DOM_interface=dom/HTMLLinkElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=
|Content=The &lt;link&gt; element allows authors to link their document to other resources. It carries the same semantics as any hyperlink, or the HTTP <code>Link:</code> header.


== Attributes ==
*<code>href</code> = URL potentially surrounded by spaces<br />Specifies a URL that provides the destination of the link.
*<code>rel</code> = set of space-separated tokens<br />Specifies a list of tokens that specify the relationship between the document containing the link and the destination indicated by the link.Two categories of links can be created using the link element: Links to external resources and hyperlinks:
*<code>media</code> = media-query list<br />The media for which the destination of the hyperlink was designed.<br />If the link is a hyperlink then the media attribute is purely advisory, and describes for which media the document in question was designed.<br />However, if the link is an external resource link, then the media attribute is prescriptive. The user agent must apply the external resource when the media attribute's value matches the environment and the other relevant conditions apply, and must not apply it otherwise.<br />The default, if the media attribute is omitted, is "all", meaning that by default links apply to all media.
* <code>hreflang</code> = language tag<br />The language of the destination of the hyperlink.<br />A valid language tag, as defined in [BCP47].
*<code>type</code> = A valid MIME type that destination of the hyperlink.<br />gives the MIME type of the linked resource.<br />The default value for the type attribute, which is used if the attribute is absent, is "text/css".
*<code>sizes</code> = icon sizes<br />The sizes attribute is used with the icon link type. The attribute must not be specified on link elements that do not have a rel attribute that specifies the icon keyword.
*Also, the title attribute has special semantics on this element. The exception is for style sheet links, where the title attribute defines alternative style sheet sets.

== Link relations ==

A URI or any IANA Link can be used as the link <code>rel=""</code>, but HTML defines special semantics for many of them:

<table class="filehistory" style="margin-left:25px; margin-top:20px;">
  <tr>
    <th>Link type</th>
    <th>Category</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>alternate</td>
    <td>Hyperlink</td>
    <td>Gives alternate representations of the current document.</td>
  </tr>
  <tr>
    <td>archives</td>
    <td>Hyperlink</td>
    <td>Provides a link to a collection of records, documents, or other materials of historical interest.</td>
  </tr>
  <tr>
    <td>author</td>
    <td>Hyperlink</td>
    <td>Gives a link to the current document's author.</td>
  </tr>
  <tr>
    <td>first</td>
    <td>Hyperlink</td>
    <td>Indicates that the current document is a part of a series, and that the first document in the series is the referenced document.</td>
  </tr>
  <tr>
    <td>help</td>
    <td>Hyperlink</td>
    <td>Provides a link to context-sensitive help.</td>
  </tr>
  <tr>
    <td>icon</td>
    <td>External Resource</td>
    <td>Imports an icon to represent the current document.</td>
  </tr>
  <tr>
    <td>index</td>
    <td>Hyperlink</td>
    <td>Gives a link to the document that provides a table of contents or index listing the current document.</td>
  </tr>
  <tr>
    <td>last</td>
    <td>Hyperlink</td>
    <td>Indicates that the current document is a part of a series, and that the last document in the series is the referenced document.</td>
  </tr>
  <tr>
    <td>license</td>
    <td>Hyperlink</td>
    <td>Indicates that the main content of the current document is covered by the copyright license described by the referenced document.</td>
  </tr>
  <tr>
    <td>next</td>
    <td>Hyperlink</td>
    <td>Indicates that the current document is a part of a series, and that the next document in the series is the referenced document.</td>
  </tr>
  <tr>
    <td>pingback</td>
    <td>External Resource</td>
    <td>Gives the address of the pingback server that handles pingbacks to the current document.</td>
  </tr>
  <tr>
    <td>prefetch</td>
    <td>External Resource</td>
    <td>Specifies that the target resource should be preemptively cached.</td>
  </tr>
  <tr>
    <td>prev</td>
    <td>Hyperlink</td>
    <td>Indicates that the current document is a part of a series, and that the previous document in the series is the referenced document.</td>
  </tr>
  <tr>
    <td>search</td>
    <td>Hyperlink</td>
    <td>Gives a link to a resource that can be used to search through the current document and its related pages.</td>
  </tr>
  <tr>
    <td>stylesheet</td>
    <td>External Resource</td>
    <td>Imports a stylesheet.</td>
  </tr>
  <tr>
    <td>sidebar</td>
    <td>Hyperlink</td>
    <td>Specifies that the referenced document, if retrieved, is intended to be shown in the browser's sidebar (if it has one).</td>
  </tr>
  <tr>
    <td>tag</td>
    <td>Hyperlink</td>
    <td>Gives a tag (identified by the given address) that applies to the current document.</td>
  </tr>
  <tr>
    <td>up</td>
    <td>Hyperlink</td>
    <td>Provides a link to a document giving the context for the current document.</td>
  </tr>
</table>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''link''' element to apply an external style sheet, called styles.css, to the page.
|Code=&lt;link rel{{=}}stylesheet href{{=}}"styles.css" type{{=}}"text/css"/&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''link''' element can be used only within the '''head''' tag.
Windows Internet Explorer 8 and later. The behavior of the [[html/attributes/href|'''href''']] and the [[html/attributes/rel|'''rel''']] attributes depends on the current document compatibility mode.

===IANA Link Relations database===
The IANA maintains a registry of valid link relations at their [http://www.iana.org/assignments/link-relations/link-relations.xhtml Link Relations registry], established in [https://tools.ietf.org/html/rfc5988 RFC5988].
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/document-metadata.html#the-link-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-link-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/links.html#edef-LINK
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=RFC 5988: Web Linking
|URL=https://tools.ietf.org/html/rfc5988
|Status=Standards Track
|Relevant_changes=
}}{{Related Specification
|Name=Subresource Integrity
|URL=http://www.w3.org/TR/SRI/
|Status=W3C Working Draft
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