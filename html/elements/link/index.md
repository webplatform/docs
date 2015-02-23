{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Stub MSDN import.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Enables the current document to establish links to external documents.}}
{{Markup_Element
|DOM_interface=dom/HTMLLinkElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
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