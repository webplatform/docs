{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines a hyperlink, a destination of hyperlink, or both.}}
{{Markup_Element
|DOM_interface=dom/HTMLAnchorElement
|Content====Description===

The <code>a</code> element defines a hyperlink to any content, which could be an external site, another page on the same site, a section within the same page, an image, or a local file.

===Syntax===

<pre><a href="[URI]">[Anchor text or image tag]</a></pre>
<pre><a id="#[identifier]">[Anchor text or image tag]</a></pre>
<pre><a>[Anchor text or image tag]</a></pre>

===Enclosed HTML===

HTML enclosed by the <code>&lt;a>&lt;/a></code> tags is typically text or an image. It is displayed in the page and (if the [[html/attributes/href|href]] attribute is present) is rendered as a link.

===Common Attributes===

{{{!}} class="wikitable"
! Name
! Value
! Purpose
! Example
! Validity
{{!}}-
{{!}} [[html/attributes/download|'''download''']]
{{!}} text
{{!}} File name to show in Save dialog
{{!}} <pre>download="filename.pdf"</pre>
{{!}} HTML5
{{!}}-
{{!}} [[html/attributes/href|'''href''']]
{{!}} [http://www.w3.org/Addressing/URL/uri-spec.html URI]
{{!}} Target of link
{{!}} <pre>href="http://example.com"</pre> <pre>href="#TableOfContents"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/id|'''id''']]
{{!}} identifier text
{{!}} Creates an anchor in the page that can be referred to by href
{{!}} <pre>id="TableOfContents"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/hreflang|'''hreflang''']]
{{!}} Language tag [http://www.ietf.org/rfc/bcp/bcp47.txt for HTML5] or [http://www.ietf.org/rfc/rfc1766.txt for HTML4]
{{!}} Hint for language of target. May be used with rel="alternate" as a hint to the server for which language to provide.
{{!}} <pre>hreflang="ja"</pre>
{{!}}-
{{!}} [[html/attributes/rel|'''rel''']]
{{!}} comma-separated list of keywords
{{!}} Indicates the relationship of the link target to the current page
{{!}} <pre>rel="help"</pre>
{{!}} &nbsp;
{{!}}-
{{!}} [[html/attributes/target|'''target''']]
{{!}} [http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword Browsing context]
{{!}} Tells where to open the link when it is followed
{{!}} <pre>target="_blank"</pre>
{{!}} &nbsp;
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- Link to an external website. -->
<a href="http://www.example.com">Example website</a>

&lt;!-- Link to an internal website in same directory. --&gt;
<a href="home.html">Home</a>

&lt;!-- Download link (HTML5 only). Value of download attribute is used as pre-filled file name in Save dialog.
    If no value is specified for the download, the name of the resource will be used.-->
<a href="filename_on_server.pdf" download="meaningful_filename.pdf">Download your pdf</a>

&lt;!-- Open a link in the window specified by the attribute TARGET. -->
<a href="http://www.example.com" target="_blank">Open example website in new window</a>

&lt;!-- Include an IMG element as a part of the link. --&gt;
<a href{{=}}"http://www.example.com"><img src="images/bullet.png">A link with an image</a>

&lt;!-- Link to an anchor on the same page. -->
<a href="#top">Go to top</a>

&lt;!-- Define an anchor. -->
<a id="top"></a>

&lt;!-- Invoke a JavaScript function (Not recommended) -->
<a href="javascript:alert('Link clicked')">Click this link</a>

&lt;!-- Links to a document and uses the ''rel'' attribute to specify the relationship to the linked document. -->
<a href="http://www.example.com/help" rel="help">Link to help</a>
|LiveURL=http://code.webplatform.org/gist/5281100
}}
}}
{{Notes_Section
|Notes====Remarks===
For creating an anchor in the page, the [[html/attributes/name|'''name''']] attribute is obsolete and should be replaced by [[html/attributes/id|'''id''']] attribute.

Both text and images can be included within an anchor. An image that is an anchor has a border whose color indicates whether the link has been visited.  To prevent this border from appearing, you can set the '''img''' element's [[html/attributes/border|'''border''']] attribute to 0 or omit the '''border''' attribute.  You can also use CSS attributes to override the default appearance of '''a''' and '''img''' elements.

The URI may refer to any protocol, e.g. http, mailto, file. A fragment (# followed by text) refers to a location in the current page. href may be omitted to indicate a placeholder link, such as a reference to the current page in a menu.

Optionally the [[html/attributes/rel|'''rel''']] element may be specified to provide semantic meaning to the link target.

Internationalization topics related to the <code>a</code> element:
* [http://www.w3.org/International/techniques/authoring-html#linkdestination Indicating the language of a link destination]
|Import_Notes====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}inline
{{!}}}

 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/2012/CR-html5-20121217/text-level-semantics.html#the-a-element
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html4/struct/links.html#edef-A
|Status=W3C Recommendation
}}{{Related Specification
|Name=WHATWG Living Standard
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/text-level-semantics.html#the-a-element
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and later
|Note=A [[html/elements/table|'''table''']] object does not function properly when contained within an '''a''' tag. The value of the [[html/attributes/href|'''href''']] attribute depends on the current document compatibility mode.  Internet Explorer 8 and later. When Protected Mode is enabled and a Web page contains an '''anchor link''' with a named [[html/attributes/target|'''target''']], Windows Internet Explorer opens the target of the link in a new window when the target has a different integrity level than the Web page containing the link. For more information, see Understanding and Working in Protected Mode Internet Explorer.
}}{{Compatibility Notes Row
|Browser=Safari / Google Chrome
|Version=any
|Note=<code>A</code> elements with href don't get focus by mouse press by default.
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/a
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}