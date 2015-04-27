{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Format HTML attributes list
User agent support per property
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The &lt;meta&gt; element embeds various kinds of metadata that cannot be expressed using the title, base, link, style, and script elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLMetaElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=none
|Content=== Attributes ==
*<code>name</code> = string<br />Sets document metadata.
**application-name<br />Giving the name of the Web application that the page represents.
**author<br />Giving the name of one of the page's authors.
**description<br />Describes the page. [[#Example_A|[Example A]]]
**generator<br />Identifies one of the software packages used to generate the document.
**keywords<br />Giving the keyword relevant to the page. [[#Example_A|[Example A]]]
Other metadata names may be registered in the WHATWG Wiki MetaExtensions page.

*<code>http-equiv</code> = string<br />When the http-equiv attribute is specified on a meta element, the element is a pragma directive.
**content-language<br />Sets the pragma-set default language.
**content-type<br />Alternative form of setting the charset attribute
**default-style<br />Sets the name of the default alternative style sheet set.
**refresh<br />Acts as timed redirect. [[#Example_B|[Example B]]]

*<code>content</code> = string<br />Gives the value of the document metadata or pragma directive when the element is used for those purposes.

*<code>charset</code> = character encoding name<br />Specifies the character encoding used by the document. [[#Example_A|[Example A]]]

== Internationalization ==
* [http://www.w3.org/International/techniques/authoring-html#indoc Declaring the character encoding for HTML]
* [http://www.w3.org/International/techniques/authoring-html#choosing Choosing and applying a character encoding]
* [http://www.w3.org/International/techniques/authoring-html#changing Changing to UTF-8]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=A minimal HTML document with meta information.
|Code=<html>
<head>
  <title>World Wide Web Consortium (W3C)</title>
  <meta charset=utf-8" />
  <meta name="description"
        content="The World Wide Web Consortium (W3C) is an international community
        where Member organizations, a full-time staff,
        and the public work together to develop Web standards." />
  <meta name="keyword" content="W3C, HTML, CSS, SVG, Web standards" />
</head>
<body></body>
</html>
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''META''' element also embeds document information that some search engines use to index and categorize documents on the World Wide Web.
This element can be used only within the '''HEAD''' element.
Windows Internet Explorer 8 or later. The behavior of the [[dom/methods/setAttribute|'''setAttribute''']] method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/document-metadata.html#the-meta-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-meta-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-META
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>content</code>
*<code>[[html/attributes/httpEquiv|httpEquiv]]</code>
*<code>Conceptual</code>
*<code>Defining Document Compatibility</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}