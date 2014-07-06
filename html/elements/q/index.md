{{Page_Title|q – quote}}
{{Flags
|State=In Progress
|Editorial notes=Add description/notes, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name|q}}
{{Summary_Section|The '''q''' element represents some phrasing content quoted from another source.}}
{{Markup_Element
|DOM_interface=dom/HTMLQuoteElement
|Content=Do not use quote characters (<code>'</code>, <code>"</code>, <code>``</code>, etc) when using the '''q''' element. If used with the [[html/elements/cite]] element, the cite must contain a valid url.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''q''' element to set apart a quotation in text.
|Code=&lt;p>She then said, &lt;q>See you around, kiddo!&lt;/q>&lt;/p>
}}{{Single Example
|Language=HTML
|Description=This example shows that the '''q''' element can have child elements.
|Code=&lt;p>Chicken Little: &lt;q>The sky is falling…
the sky is falling… &lt;em>the sky is falling!&lt;/em>&lt;/q>&lt;/p>
}}
}}
{{Notes_Section
|Usage=The '''q''' should be used to denote short, inline quotes that do not need a paragraph of their own.
For longer quotes, please use the [[html/elements/blockquote|'''blockquote''']] element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/html/wg/drafts/html/master/text-level-semantics.html#the-cite-element
|Status=W3C Editor's Draft
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
|Manual_links=* [[html/elements/cite|<code>cite</code>]]
* [[html/elements/blockquote|<code>blockquote</code>]]
}}
{{Topics|HTML, Usability}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}