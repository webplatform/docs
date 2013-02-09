{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''h1''' through '''h6''' elements define levels of headings within a document.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- 
    The H1 element applies a
    level-1 heading syle to the
    contained text. 
--&gt;
&lt;h1&gt;Welcome to Web Platform Docs!&lt;/h1&gt;

&lt;!-- 
    H2 is used for level-2 headings.
 --&gt;
&lt;h2&gt;Introduction&lt;/h2&gt;

&lt;!-- etc. --&gt;
&lt;h3&gt;Prologue&lt;/h2&gt;
&lt;h4&gt;Level-4 Heading&lt;/h4&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Use H1 through H6 to specify different sizes and styles of headings.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.5.5


===HTML information===
|class="wikitable"
|}===Members===
The '''hn''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''hn''' object has these events.
{
|}
 ====Properties====
The '''hn''' object has these properties.
{
|Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes_ [[dom/traversal/properties/childElementCount|'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|'''nodeType''']] {{=}}1, or element nodes.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}