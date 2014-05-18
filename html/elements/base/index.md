{{Page_Title}}
{{Flags
|High-level issues=Data Not Semantic
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''base''' element is used to specify a document's base URL and base target that is used for resolving relative URLs within the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLBaseElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px"><em>none</em></td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Only permitted to occur once within [[html/elements/head|<code>&lt;head&gt;</code>]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A <code>&lt;base&gt;</code> element must not have an end tag.</td>
</tr>
</table>

A relative URL (<var>some/example.html</var>) needs to be transformed to a fully qualified URL (<var>http://example.org/some/example.html</var>) before it can be downloaded. Usually the document's URL (available to JavaScript through the [[dom/Location|<code>location</code>]] object) is used as the base URL for resolving relative URLs. The <code>&lt;base&gt;</code> element allows you to override this default with the [[html/attributes/href|<code>href</code>]] attribute.

Links ([[html/elements/a|<code>&lt;a&gt;</code>]]) and forms ([[html/elements/form|<code>&lt;form&gt;</code>]]) open in a ([[html/attributes/target|<code>target</code>]]). The default target is <var>_self</var>, resulting in the link opening in the same window as the document currently viewed. This default can be overridden document-wide using <code>&lt;base target="…"&gt;</code>.

If a document is integrated in an [[html/elements/iframe|<code>iframe</code>]], it may help to specify <code>&lt;base target="_parent"&gt;</code> in order to open the links within the iframe in the scope parent document. If <var>_parent</var> or <var>_top</var> are used without the document really being integrated in an hierarchy, expect the behavior of <var>_self</var>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows a link with the relative destination <var>some-file.html</var> that gets rewritten to <var>http://example.org/deep/some-file.html</var>
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;base element example&lt;/title&gt;
    &lt;base href="http://www.example.org/deep/"&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;A &lt;a href="some-file.html"&gt;relative link&lt;/a&gt;.&lt;/p&gt;
    &lt;!-- after resolving the above link equals to --&gt;
    &lt;p&gt;A &lt;a href="http://www.example.org/deep/some-file.html"&gt;relative link&lt;/a&gt;.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=HTML
|Description=The example shows that '''base''' only affects elements following it
|Code=&lt;head&gt;
  &lt;title&gt;base element example&lt;/title&gt;
  &lt;link href="my-style.css&quot; rel="stylesheet"&gt;
  &lt;base href="http://example.com"&gt;
  &lt;link href="my-other-style.css" rel="stylesheet"&gt;
  &lt;!--
    resolves to
    [current domain and directory]/my-style.css
    http://example.com/my-other-style.css
  --&gt;
&lt;/head&gt;
}}{{Single Example
|Language=HTML
|Description=The example shows how multiple '''base''' occurrences are collapsed and ignored
|Code=&lt;head&gt;
  &lt;title&gt;base element example&lt;/title&gt;
  &lt;base href="http://example.com"&gt;
  &lt;base target="_blank"&gt;
  &lt;base href="http://webplatform.org" target="_top"&gt;
  &lt;!--
    equals to the single definition:
    &lt;base href="http://example.com/" target="_blank"&gt;
    except for Internet Explorer, where only the first element is read:
    &lt;base href="http://example.com/" target="_self"&gt;    
  --&gt;
&lt;/head&gt;
}}
}}
{{Notes_Section
|Notes=* Relative URLs within <code>&lt;base&gt;</code> don't work in every browser, resolving a relative base URL was introduced in Firefox 4 and Internet Explorer 10.
* <code>&lt;base&gt;</code> only affects elements following it's declaration.
* multiple <code>&lt;base&gt;</code> declarations are illegal, only the ''first'' [[html/attributes/href|<code>href</code>]] and [[html/attributes/target|<code>target</code>]] are used, the rest is discarded. Internet Explorer ignores all <code>&lt;base&gt;</code> instances after the first.

'''Note''' Inline SVGs using references like <code>fill="url(#element-id)"</code> can be a problem in documents using <code>&lt;base&gt;</code>. The reason is that <code>url(#element-id)</code> is actually a URL, not a CSS selector. At least Firefox and Chrome are susceptible to this behavior.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/struct/links.html#h-12.4
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-base-element.html#the-base-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=WHATWG
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#the-base-element
|Status=Living Standard
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/base Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535191%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}