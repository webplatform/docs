{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''dd''' element (&lt;dd&gt;) represents the description, definition, or value, part of a term-description group in a description list ([[html/elements/dl|&lt;dl&gt;]] element).}}
{{Markup_Element
|DOM_interface=dom/HTMLDDElement
|Content====HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|block
|}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''dd''' element with the '''dl''' and '''dt''' elements to create a definition list.
|Code=&lt;dl&gt;
  &lt;dt&gt;Cat&lt;/dt&gt;
  &lt;dd&gt;A small domesticated mammal.&lt;/dd&gt;
  &lt;dt&gt;Lizard&lt;/dt&gt;
  &lt;dd&gt;A reptile generally found in dry areas.&lt;/dd&gt;
&lt;/dl&gt;
}}
}}
{{Notes_Section|}
 ====Properties====
The '''dd''' object has these properties.
{
|class="wikitable"
|Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes_ [[dom/traversal/properties/childElementCount|'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|'''nodeType''']] {{=}}1, or element nodes.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/struct/lists.html#h-10.3
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-dd-element.html#the-dd-element
|Status=W3C Working Draft
}}
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
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}