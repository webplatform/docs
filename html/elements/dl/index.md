{{Page_Title|dl – description list}}
{{Flags
|State=In Progress
|Editorial notes=Add Category and Compatibility information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|dl}}
{{Summary_Section|The '''dl''' element is used to define a '''description list'''. The element encloses one or more '''description terms''', enclosed in [[html/elements/dt|'''dt''']] elements, and '''description definitions''' (definitions of the terms), enclosed within [[html/elements/dd|'''dd''']] elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLDListElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">One of the following:
* Either: Zero or more groups each consisting of one or more [[html/elements/dt|'''dt''']] elements followed by one or more [[html/elements/dt|'''dd''']] elements.
* Or: A [[html/elements/template|'''template''']] element.
* Or: A [[html/elements/template|'''template''']] element or a [[html/elements/dt|'''dt''']] element, followed by zero or more [[html/elements/template|'''template''']], [[html/elements/dt|'''dt''']], and [[html/elements/dd|'''dd''']] elements, followed by a [[html/elements/template|'''template''']] element or a [[html/elements/dd|'''dd''']] element.</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Any element that can contain [[html/concepts/flowContent|flow content]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A '''dl''' element must have both a start tag and an end tag.</td>
</tr>
</table>

The '''dl''' element is often useful to create a semantic list of terms and their definitions, whether these are name value pairs, glossary terms and definitions, or anything other items that fit this pattern. '''Description lists''' allow you to do this easily inside HTML.

A description list is always wrapped by a single '''dl''' element. Inside that element you can place any number of child [[html/elements/dt|'''description topics''']], inside '''dt''' elements, and [[html/elements/dd|'''description definitions''']] — the description or definition of the specified terms or topics — inside '''dd''' elements.

It doesn't make sense to have an item without a description, or the other way round, but note that it is acceptable to have a single item with multiple descriptions, or a description with multiple items (see code examples section.)

The topics should always be placed before the descriptions.

A description list is not used as commonly as other types of list, except in journals, research papers, and other documentation  where item/value pairs need to be displayed. For other uses, they are often not used as they are considered more difficult to style than other list types.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a simple definition list with two item/description pairs.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
  &lt;dt&gt;Coca Cola&lt;/dt&gt;
  &lt;dd&gt;One of the leading brands of a popular cold fizzy drink.&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=This example shows a definition list with a single item but multiple descriptions for that item.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
  &lt;dd&gt;A mid brown colour&lt;/dd&gt;
  &lt;dd&gt;A common social invitation&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=This example shows a definition list with a single description and multiple items fitting that description.
|Code=&lt;dl&gt;
  &lt;dt&gt;Coffee&lt;/dt&gt;
  &lt;dt&gt;Tea&lt;/dt&gt;
  &lt;dt&gt;Vimto (in the North of England)&lt;/dt&gt;
  &lt;dd&gt;A popular hot drink.&lt;/dd&gt;
&lt;/dl&gt;
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the '''dl''' element.
|Code=display: block;
margin-top: 16px;
margin-bottom: 16px;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-dl-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/lists.html#edef-DL
|Status=W3C Recommendation
|Relevant_changes=
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
|Manual_links=* [[html/elements/dir|<code>dir</code>]]
* [[html/elements/menu|<code>menu</code>]]
* [[html/elements/ol|<code>ol</code>]]
* [[html/elements/ul|<code>ul</code>]]
* [[html/elements/li|<code>li</code>]]
* [[html/elements/dt|<code>dt</code>]]
* [[html/elements/dd|<code>dd</code>]]
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/dl Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535241%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}