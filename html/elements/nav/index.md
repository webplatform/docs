{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent and Children information. Complete Compatibility table.
|Checked_Out=No
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The HTML Navigation Element (<nav>) represents a section of a page that links to other pages or to parts within the page: a section with navigation links}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}block
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example uses the '''nav''' element to indicate that a list contains site navigation links.
|Code=&lt;nav&gt;
 &lt;h1&gt;Site Navigation&lt;/h1&gt;
 &lt;ul&gt;
  &lt;li&gt;&lt;a href{{=}}"index.html"&gt;Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href{{=}}"gallery.html"&gt;Photo&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href{{=}}"news.html"&gt;Updates&lt;/a&gt;&lt;/li&gt;
 &lt;/ul&gt;
&lt;/nav&gt;
}}
}}
{{Notes_Section
|Usage=Not all groups of links on a document need to be in a '''nav''' element, only sections that consist of major navigation blocks. In particular, it is common for '''footer''' elements to have a short list of links to various documents of a site, such as the terms of service, home, and copyright. The '''footer''' element alone is sufficient for such cases, and does not require a '''nav''' element.

'''Note'''  Some devices and applications (such as screen readers) might use the '''nav''' element as a way to determine what content on the document to initially skip or provide on request.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-nav-element.html#the-nav-element
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=4
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=11
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=The '''nav''' element is only supported for webpages displayed in IE9 Standards mode.
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}