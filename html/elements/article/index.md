{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete,  Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=An '''article''' element might represent a forum post, a magazine or newspaper article, a blog entry, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.
When '''article''' elements are nested, the inner article should be related to the contents of the outer article. For example, a blog entry on a site that accepts user-submitted comments might represent the comments as '''article''' elements nested within the '''article''' element for the blog entry.

===HTML information===
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
|Description=The following example shows the basic structure of an article using '''article''', '''header''', and '''footer''' elements.
|Code=&lt;article&gt;
 &lt;header&gt;
  &lt;h1&gt;Article Heading&lt;/h1&gt;
 &lt;/header&gt;
 &lt;p&gt;Article Text&lt;/p&gt;
 &lt;p&gt;...&lt;/p&gt;
 &lt;footer&gt;Article Footer&lt;/footer&gt;
&lt;/article&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/the-article-element.html#the-article-element
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=21
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=The '''article''' element is only supported for webpages displayed in IE9 Standards mode. Internet Explorer 9 does not natively support the '''time''' element, which is intended to provide the publication date of the article element.
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