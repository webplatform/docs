{{Page_Title|dt – description list topic}}
{{Flags
|State=In Progress
|Editorial notes=Add Category and Compatibility information. Modify/Complete Parent and Children information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|dt}}
{{Summary_Section|The '''dt''' element indicates a definition term within a definition list ([[html/elements/dl|'''dl''']]). 

A [[html/elements/dt|'''dt''']] (topic) is usually followed by one or more [[html/elements/dd|'''dd''']] (definition) elements. Several consecutive [[html/elements/dt|'''dt''']] are attributed to the [[html/elements/dd|'''dd''']] element that immediately follows the group.
}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">[[html/concepts/flowContent|flow content]], but with no [[html/elements/header|header]], [[html/elements/footer|footer]], [[html/concepts/sectioningContent|sectioning content]], or [[html/concepts/headingContent|heading content]] descendants.</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>[[html/elements/dl|dl]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A '''dt''' element's end tag may be omitted if the '''dt''' element is immediately followed by another '''dt''' element or a '''dd''' element.</td>
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
|Description=Typical browser default CSS properties for the '''dt''' element.
|Code=display: block;
}}
}}
{{Notes_Section
|Notes=The [[html/elements/dt|dt]] element itself, when used in a [[html/elements/dl|dl]] element, does not indicate that its contents are a term being defined, but this can be indicated using the [[html/elements/dfn|dfn]] element.

While [[dom/HTMLDTElement|HTMLDTElement]] is the defined DOM interface for this element, most browsers currently use [[dom/HTMLElement|HTMLElement]] instead.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-dt-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-dt-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/lists.html#edef-DT
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
* [[html/elements/dd|<code>dd</code>]]
* [[html/elements/dl|<code>dl</code>]]
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/dt Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535243%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}