{{Page_Title|dd – description list data}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|dd}}
{{Summary_Section|The <code>&lt;dd&gt;</code> element represents the description, definition, or value, part of a term-description group in a definition list ([[html/elements/dl|<code>&lt;dl&gt;</code>]]). 

A [[html/elements/dt|<code>&lt;dt&gt;</code>]] (topic) is usually followed by one or more [[html/elements/dd|<code>&lt;dd&gt;</code>]] (definition) elements. Several consecutive [[html/elements/dt|<code>&lt;dt&gt;</code>]] are attributed to the [[html/elements/dd|<code>&lt;dd&gt;</code>]] element that immediately follows the group.
}}
{{Markup_Element
|DOM_interface=dom/HTMLDDElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">[[html/concepts/flowContent|flow content]].</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>[[html/elements/dl|dl]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A <code>&lt;dl&gt;</code> element must have both a start tag and an end tag.</td>
</tr>
</table>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows a simple definition list with two item/description pairs.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
  &lt;dt&gt;Coca Cola&lt;/dt&gt;
  &lt;dd&gt;One of the leading brands of a popular cold fizzy drink.&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=The example shows a definition list with a single item but multiple descriptions for that item.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
  &lt;dd&gt;A mid brown colour&lt;/dd&gt;
  &lt;dd&gt;A common social invitation&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=The example shows a definition list with a single description and multiple items fitting that description.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dt&gt;Tea&lt;/dt&gt;
  &lt;dt&gt;Vimto (in the North of England)&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the <code>&lt;dd&gt;</code> element.
|Code=display: block;
margin-left: 40px;
}}
}}
{{Notes_Section
|Notes=While [[dom/HTMLDTElement|HTMLDTElement]] is the defined DOM interface for this element, most browsers currently use [[dom/HTMLElement|HTMLElement]] instead.
|}
 ====Properties====
The '''dd''' object has these properties.
{
|class="wikitable"
|Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes_ [[dom/traversal/properties/childElementCount|'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|'''nodeType''']] {{=}}1, or element nodes.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/lists.html#h-10.3
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/grouping-content.html#the-dd-element
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
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
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/dd Mozilla Developer Network]
* [http://msdn.microsoft.com/en-US/library/ie/ms535234.aspx Microsoft Developer Network]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}