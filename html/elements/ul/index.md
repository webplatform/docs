{{Page_Title|ul – unordered list}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|ul}}
{{Summary_Section|The '''ul''' element is used to define an '''unordered list'''. The element encloses one or more '''list items''', enclosed in [[html/elements/li|'''li''']] elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLUListElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">One of the following:
* Either: Zero or more [[html/elements/li|'''li''']] elements.
* Or: A [[html/elements/template|'''template''']] element.
* Or: any combination of the above two  
</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Any element that can contain [[html/concepts/flowContent|flow content]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A '''ul''' element must have both a start tag and an end tag.</td>
</tr>
</table>


The '''unordered list''', represented by the '''ul''' element, is most often used to group a list of items, enclosed in [[html/elements/li|'''li''']] elements, together in a semantic way. Usually, the order in which the items are presented is not important.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''ul''' element to create a bulleted list.
|Code=<nowiki><ul>
  <li>Alice</li>
  <li>Bob</li>
  <li>Carol</li>
</ul></nowiki>
}}{{Single Example
|Language=HTML
|Description=Example with nested lists
|Code=<nowiki><ul>
  <li>Alice <ul>
    <li>Red</li>
    <li>Green</li>
  </ul>
  </li>
  <li>Bob <ul>
    <li>Green</li>
    <li>Cyan</li>
  </ul></li>
  <li>Carol <ul>
    <li>Magenta</li>
    <li>Yellow</li>
  </ul></li>
</ul></nowiki>
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the '''ul''' element.
|Code=display: block;
list-style-type: disc;
margin-top: 16px;
margin-bottom: 16px;
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[html/attributes/type (ul,li,ol elements)|'''type''']] attribute sets the list type for all ensuing lists unless a different type value is set.
The '''ul''' element inherits its [[css/properties/line-height|'''line-height''']] from the height of the [[css/properties/font|'''font''']] attribute for the '''body'''. For example, if the [[css/properties/font-size|'''font-size''']] attribute for the '''body''' is larger than the '''font-size''' attribute for the '''ul''' element, the list items in the '''ul''' are spaced according to the '''font-size''' of the '''body'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-ul-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-ul-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/lists.html#edef-UL
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_links=* [[html/elements/dir|<code>dir</code>]]
* [[html/elements/menu|<code>menu</code>]]
* [[html/elements/ol|<code>ol</code>]]
* [[html/elements/li|<code>li</code>]]
* [[html/elements/dl|<code>dl</code>]]
* [[html/elements/dt|<code>dt</code>]]
* [[html/elements/dd|<code>dd</code>]]
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