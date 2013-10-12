{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>&lt;base&gt;</code> element is used to specify a document's base URL and base target that is used for resolving relative URLs within the document.}}
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

A relative URL (<var>some/example.html</var>) needs to be transformed to a fully qualified URL (<var>http://example.org/some/example.html</var>) before it can be downloaded. Usually the document's URL (available to JavaScript through the [[dom/location|<code>location</code>]] object) is used as the base URL for resolving relative URLs. The <code>&lt;base&gt;</code> element allows you to override this default with the [[html/attributes/href|<code>href</code>]] attribute.

Links ([[html/elements/a|<code>&lt;a&gt;</code>]]) and ([[html/elements/form|<code>&lt;form&gt;</code>]]) open in a ([[html/attributes/target|<code>target</code>]]). The default target is <var>_self</var>, resulting in the link opening in the same window as the document currently viewed. This default can be overridden document-wide using <code>&lt;base target="…"&gt;</code>.

If a document is integrated in an [[html/attributes/iframe|<code>iframe</code>]], it may help to specify <code>&lt;base target="_parent"&gt;</code> in order to open the links within the iframe in the scope parent document. If <var>_parent</var> or <var>_top</var> are used without the document really being integrated in an hierarchy, expect the behavior of <var>_self</var>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows a link with the relative destination <var>some-file.html</var> that gets rewritten to <var>http://example.org/deep/some-file.html</var>
|Code=&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;base element example&lt;/title&gt;
    &lt;base href=&quot;http://www.example.org/deep/&quot;&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;A &lt;a href=&quot;some-file.html&quot;&gt;relative link&lt;/a&gt;.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=HTML
|Description=The example shows a link that is opened in a new window (or tab)
|Code=&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;base element example&lt;/title&gt;
    &lt;base target=&quot;blank&quot;&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;A &lt;a href=&quot;some-file.html&quot;&gt;relative link&lt;/a&gt;.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Usage=TODO: Relative URLs aren't supported reliably across browsers. It was added as late as Firefox 4 …
TODO: <svg> and url(#foo) problem

TODO: explain multiple occurrence, and that it only applies AFTER the fact - use examples for this
|Notes====Remarks===
When used, the '''base''' element must appear within the '''head''' of the document, before any elements that refer to an external source.
If more than one '''base''' element occurs,  only the first element will be recognized.
Windows Internet Explorer 8 and later. When read, the value of the [[html/attributes/href (base)|'''href''']] attribute depends on the current document compatibility mode.  In addition, relative URL's are no longer supported by the '''base''' element.
'''Note'''   Versions of Windows Internet Explorer prior to Windows Internet Explorer 7 would allow the '''base''' element to appear anywhere in the document tree, which caused relative paths to use the "nearest" '''base''' element as the base for the URL. Internet Explorer 7 strictly enforces the use of the '''base''' tag within the '''head''' of the document, and will ignore misplaced tags.
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
|Topic_clusters=HTML
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