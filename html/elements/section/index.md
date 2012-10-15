{{Page_Title}}
{{Flags
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section}}
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


A section  is a thematic grouping of content, typically with a heading. Examples of sections would be chapters, the various tabbed pages in a tabbed dialog box, or the numbered sections of a thesis. A website's home page could be split into sections for an introduction, news items, and contact information.
The '''section''' element is not a generic container element. Authors are encouraged to use the '''div''' element for styling purposes or when an element is needed as a convenience for scripting. The '''section''' element is appropriate only if the element's contents would be listed explicitly in the document's outline.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, an '''article''' (part of a larger document about apples) contains two short sections.
|Code=&lt;article&gt;
 &lt;hgroup&gt;
  &lt;h1&gt;Apples&lt;/h1&gt;
  &lt;h2&gt;Tasty, delicious fruit!&lt;/h2&gt;
 &lt;/hgroup&gt;
 &lt;p&gt;The apple is the pomaceous fruit of the apple tree.&lt;/p&gt;
 &lt;section&gt;
  &lt;h1&gt;Red Delicious&lt;/h1&gt;
  &lt;p&gt;These bright red apples are the most common found in many
  supermarkets.&lt;/p&gt;
 &lt;/section&gt;
 &lt;section&gt;
  &lt;h1&gt;Granny Smith&lt;/h1&gt;
  &lt;p&gt;These juicy, green apples make a great filling for
  apple pies.&lt;/p&gt;
 &lt;/section&gt;
&lt;/article&gt;
}}{{Single Example
|Language=HTML
|Description=The rank of '''h1-h6''' elements is determined by the number in their name.  The '''h1''' element is said to have the highest rank; the '''h6''' element has the lowest rank.  Two elements with the same name have the same rank. The default style applied to '''hn''' elements varies according to the rank of the element. However, the rank of headings that appear within a '''section''' element is automatically reduced.  This affects the visual appearance of the headings inside the '''section''' element. In the following example, the author uses '''h1''' elements without worrying whether a particular section is at the top level, the second level, the third level, and so on. The two outlines produce equivalent output.
|Code=&lt;!-- First outline --&gt;
&lt;h1&gt;Let's call it a draw(ing surface)&lt;/h1&gt;
&lt;h2&gt;Diving in&lt;/h2&gt;
&lt;h2&gt;Simple shapes&lt;/h2&gt;
&lt;h2&gt;Canvas coordinates&lt;/h2&gt;
&lt;h3&gt;Canvas coordinates diagram&lt;/h3&gt;
&lt;h2&gt;Paths&lt;/h2&gt;
&lt;hr/&gt;
&lt;!-- Equivalent outline using section elements --&gt;
&lt;h1&gt;Let's call it a draw(ing surface)&lt;/h1&gt;
&lt;section&gt;
&lt;h1&gt;Diving in&lt;/h1&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Simple shapes&lt;/h1&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Canvas coordinates&lt;/h1&gt;
&lt;section&gt;
&lt;h1&gt;Canvas coordinates diagram&lt;/h1&gt;
&lt;/section&gt;
&lt;/section&gt;
&lt;section&gt;
&lt;h1&gt;Paths&lt;/h1&gt;
&lt;/section&gt;
}}
}}
{{Notes_Section
|Usage='''Note'''  Authors are encouraged to use the '''[[html/elements/article|article]]''' element instead of the '''section''' element when it would make sense to syndicate the contents of the element.
|Notes=


}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/the-section-element.html#the-section-element
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=Windows Internet Explorer 9.  The '''section''' element is only supported for webpages displayed in IE9 Standards mode.
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