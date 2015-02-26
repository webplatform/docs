{{Page_Title|EMBED}}
{{Flags
|State=In Progress
|Editorial notes=Add history of the element
Add Category, Parent, Children and Compatibility information.
|Checked_Out=Yes
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete, Examples Needed, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The HTML &lt;embed&gt; Element represents an integration point for an external content- typically, non-HTML content such as an application or some other type of interactive content which involves use of a third-party plugin as a handler (rather than being natively supported by the UA).}}
{{Markup_Element
|DOM_interface=dom/HTMLEmbedElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=inline-block
|Content=
== Accessibility ==
Authors should ensure that the information and user interface components must be presentable to users in ways they can perceive ([http://www.w3.org/TR/WCAG20/#perceivable WCAG 2.0 - Principle 1: Perceivable]). This includes providing alternatives for time-based media [http://www.w3.org/TR/WCAG20/#media-equiv Guideline 1.2].


== HTML Attributes ==
*<code>src</code> = URL potentially surrounded by spaces<br />gives the address of the resource being embedded.
*<code>type</code> = MIME type<br />Specifies the type of the resource.
*<code>width</code> = non-negative integer<br />Give the width of the visual content of the element, in CSS pixels.
*<code>height</code> = non-negative integer<br />Give the height of the visual content of the element, in CSS pixels.

== History ==

While only being formalized as of HTML5, the tag has been informally supported among some user-agents as far back as Netscape Navigator 2.0 [http://lists.w3.org/Archives/Public/www-talk/1995SepOct/0045.html]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following use of the '''EMBED''' element mimics the behavior of the '''BGSOUND''' tag.
|Code=&lt;EMBED type{{=}}"audio/x-midi" src{{=}}"BackInTheSaddle.mid" hidden{{=}}"true"&gt;
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Way to embed a resource that requires a proprietary plugin, like Flash.If the user does not have the plugin (for example if the plugin vendor doesn't support the user's platform), then the user will be unable to use the resource.
|Code=&lt;Embed src="catgame.swf"&gt;
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=To pass the plugin a parameter "quality" with the value "high", an attribute can be specified:
|Code=&lt;Embed src="catgame.swf" quality="high"&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The interactive element embed must not appear as a descendant of the a element.
The interactive element embed must not appear as a descendant of the button element.
The name attribute on the embed element is obsolete. Use the id attribute instead.
The align attribute on the embed element is obsolete. Use CSS instead.
The hspace attribute on the embed element is obsolete. Use CSS instead.
The vspace attribute on the embed element is obsolete. Use CSS instead.
|Notes====Remarks===
The '''EMBED''' element must appear inside the '''BODY''' element of the document.
Users need to have an application that can view the data installed on their computer.
'''Tip:  ''' In some cases, you may achieve better results by adding the file name extension of the add-on as a query parameter to the file name specified in the [[html/attributes/src (iframe, embed, xml)|'''SRC''']] attribute. 

Permitted attributes -
global attributes,& src ,& type, & height, & width, & Any other attribute that has no namespace.

Permitted parent elements
Any element that can contain phrasing elements
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-embed-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-embed-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Multimedia, Video
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|Audio, HTML, Media, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}