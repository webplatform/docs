{{Page_Title|ol – ordered list}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name|ol}}
{{Summary_Section|The '''ol''' element is used to define an '''ordered list'''. The element encloses one or more '''list items''', enclosed in [[html/elements/li|'''li''']] elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLOListElement
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
<td>A '''ol''' element must have both a start tag and an end tag.</td>
</tr>
</table>

The '''ordered list''', represented by the '''ol''' element, is most often used to group a list of items, enclosed in [[html/elements/li|'''li''']] elements, together in an ordered and semantic way.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''ol''' element to create a numbered list.
|Code=&lt;ol&gt;
&nbsp;&nbsp;&lt;li&gt;This&nbsp;is&nbsp;the&nbsp;first&nbsp;list&nbsp;item&lt;/li&gt;
&nbsp;&nbsp;&lt;li&gt;This&nbsp;is&nbsp;the&nbsp;second&nbsp;list&nbsp;item&lt;/li&gt;
&lt;/ol&gt;
|LiveURL=http://code.webplatform.org/gist/eb2b4134dc595b6dbf17
}}{{Single Example
|Language=HTML
|Description=The '''ol''' element with the '''type''' attribute set to '''a'''.
|Code=&lt;ol&nbsp;type=&quot;a&quot;&gt;
&nbsp;&nbsp;&lt;li&gt;This&nbsp;is&nbsp;the&nbsp;first&nbsp;list&nbsp;item&lt;/li&gt;
&nbsp;&nbsp;&lt;li&gt;This&nbsp;is&nbsp;the&nbsp;second&nbsp;list&nbsp;item&lt;/li&gt;
&lt;/ol&gt;
|LiveURL=http://code.webplatform.org/gist/3386252885e8db151a1f
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the '''ol''' element.
|Code=display: block;
list-style-type: decimal;
margin-top: 16px;
margin-bottom: 16px;
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[html/attributes/type (ul,li,ol elements)|'''type''']] attribute sets the list type for all ensuing lists unless a different type value is set.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 10.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-ol-element
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=1.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=1.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=reversed attribute
|Chrome_supported=Yes
|Chrome_version=18.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=18.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.2
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
|Firefox_mobile_version=1.0
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
}}{{Compatibility Table Mobile Row
|Feature=reversed attribute
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=* [[html/elements/dir|<code>dir</code>]]
* [[html/elements/menu|<code>menu</code>]]
* [[html/elements/ul|<code>ul</code>]]
* [[html/elements/li|<code>li</code>]]
* [[html/elements/dl|<code>dl</code>]]
* [[html/elements/dt|<code>dt</code>]]
* [[html/elements/dd|<code>dd</code>]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}