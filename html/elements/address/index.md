{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add syntax, attribute, example, compatibility.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''address''' element (&lt;address&gt;) encloses contact information of the owner or the author of the document or the article.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''address''' element to make text appear in italic type.
|Code=<!-- This is just a snippet, not a full page. -->
&lt;address&gt;This text will be in italic type.&lt;/address&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Webkit (Safari, old Android and similar) and Trident (Internet Explorer) user agent default style -
<pre>address {
	display:block;
	font-style: italic;
}</pre>
Gecko (Firefox) user agent default style -
<pre>address, address[dir]{
         unicode-bidi: -moz-isolate;
         display:block;
         font-style:italic;
}</pre>
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.5.6


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
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
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