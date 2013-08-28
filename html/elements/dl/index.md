{{Page_Title|dl – description list}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|dl}}
{{Summary_Section|The <code>&lt;dl&gt;</code> element is used to define a '''description list'''. The element encloses one or more '''description terms''', enclosed in [[html/elements/dt|<code>&lt;dt&gt;</code>]] elements, and '''description definitions''' (definitions of the terms), enclosed within [[html/elements/dd|<code>&lt;dd&gt;</code>]] elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLDListElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">One of the following:
* Either: Zero or more groups each consisting of one or more [[html/elements/dt|<code>&lt;dt&gt;</code>]] elements followed by one or more [[html/elements/dt|<code>&lt;dd&gt;</code>]] elements.
* Or: A [[html/elements/template|<code>&lt;template&gt;</code>]] element.
* Or: A [[html/elements/template|<code>&lt;template&gt;</code>]] element or a [[html/elements/dt|<code>&lt;dt&gt;</code>]] element, followed by zero or more [[html/elements/template|<code>&lt;template&gt;</code>]], [[html/elements/dt|<code>&lt;dt&gt;</code>]], and [[html/elements/dd|<code>&lt;dd&gt;</code>]] elements, followed by a [[html/elements/template|<code>&lt;template&gt;</code>]] element or a [[html/elements/dd|<code>&lt;dd&gt;</code>]] element.</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Any element that can contain [[html/concepts/flowContent|flow content]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A <code>&lt;dl&gt;</code> element must have both a start tag and an end tag.</td>
</tr>
</table>

The <code>&lt;dl&gt;</code> element is often useful to create a semantic list of terms and their definitions, whether these are name value pairs, glossary terms and definitions, or anything other items that fit this pattern. '''Description lists''' allow you to do this easily inside HTML.

A description list is always wrapped by a single <code>&lt;dl&gt;</code> element. Inside that element you can place any number of child '''description items''' — the items to be described or defined — inside <code>&lt;dt&gt;</code> elements, and '''description definitions''' — the description or definition of the specified items — inside <code>&lt;dd&gt;</code> elements.

It doesn't make sense to have an item without a description, or the other way round, but note that it is acceptable to have a single item with multiple descriptions, or a description with multiple items (see code examples section.)

The items should always be placed before the descriptions.

A description list is not used as commonly as other types of list, except in journals, research papers, and other documentation  where item/value pairs need to be displayed. For other uses, they are often not used as they are considered more difficult to style than other list types.
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
|Description=Typical browser default CSS properties for the <code>&lt;dl&gt;</code> element.
|Code=display: block;
margin-top: 16px;
margin-bottom: 16px;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/lists.html#h-10.3
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/grouping-content.html#the-dl-element
|Status=W3C Editor's Draft
|Relevant_changes=In HTML5, definition list has been changed to description list
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
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/dl Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535241%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}