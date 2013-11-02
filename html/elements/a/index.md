{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a hyperlink or anchor.}}
{{Markup_Element
|DOM_interface=dom/HTMLAnchorElement
|Content====Description===

Defines a hyperlink to any content, which could be an external site, another page on the same site, a section within the same page, an image, or a local file. It may even invoke a JavaScript function.

===Syntax===

<pre><a href="[URI]">[Anchor text or image tag]</a></pre>
<pre><a id="#[identifier]">[Anchor text or image tag]</a></pre>
<pre><a>[Anchor text or image tag]</a></pre>

===Inner HTML===

The inner HTML is the enclosed anchor text or image tag, which is displayed in the page and (if href is present) is rendered as a link.

===Value===

(Rarely used.)

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
{{!}} [http://www.w3.org/Addressing/URL/uri-spec.html URI] enclosed in double-quotes
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
{{!}} <pre>reflang="ja"</pre>
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

===Other Attributes===

{{{!}} class="wikitable"
! Name
! Value
! Purpose
! Example
! Validity
{{!}}-
{{!}} [[html/attributes/rel|'''rel''']]
{{!}} text
{{!}} Indicates the relationship of the current page to the link target
{{!}} <pre>rev="index"</pre>
{{!}} removed in HTML5
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the '''a''' element to link to files, open a file, include an image as part of a link, define an anchor, and invoke a function.
|Code=&lt;!-- Link to an external website. --&gt;
&lt;a href{{=}}"http://www.example.com"&gt;Example website&lt;/a&gt;

&lt;!-- Link to an internal website in same directory. --&gt;
&lt;a href{{=}}"home.html"&gt;Home&lt;/a&gt;

&lt;!-- Download link (HTML5 only). Value of download attribute is used as pre-filled file name in Save dialog --&gt;
&lt;a href{{=}}"filename_on_server.pdf" download="meaningful_filename.pdf"&gt;Download your pdf&lt;/a&gt;

&lt;!-- Open a link in the window specified by the attribute TARGET. --&gt;
&lt;a href{{=}}"http://www.example.com" target{{=}}"_blank"&gt;Open example website in new window&lt;/a&gt;

&lt;!-- Include an IMG element as a part of the link. --&gt;
&lt;a href{{=}}"http://www.example.com"&gt;&lt;img src{{=}}"images/bullet.png"&gt;A link with an image&lt;/a&gt;

&lt;!-- Link to an anchor on the same page. --&gt;
&lt;a href{{=}}"#top"&gt;Go to top&lt;/a&gt;

&lt;!-- Define an anchor. --&gt;
&lt;a id{{=}}"top"&gt;

&lt;!-- Invoke a JavaScript function (Not recommended) --&gt;
&lt;a href{{=}}"javascript:alert('Link clicked')"&gt;Click this link&lt;/a&gt;

&lt;!-- Links to a document and uses the ''rel'' attribute to specify the relationship to the linked document. --&gt;
&lt;a href{{=}}"http://www.example.com/help" rel{{=}}"help"&gt;Link to help&lt;/a&gt;
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
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Working Draft
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
{{See_Also_Section
|External_links=* [http://www.w3.org/TR/html4/struct/links.html#edef-A HTML 4.01 specification]
* [http://www.w3.org/TR/2012/CR-html5-20121217/text-level-semantics.html#the-a-element HTML 5 specification]
* [http://www.whatwg.org/specs/web-apps/current-work/multipage/text-level-semantics.html#the-a-element WHATWG specification]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/a
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}