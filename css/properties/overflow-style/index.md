{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=auto
|Applies to=non-replaced block-level elements and non-replaced inline-block elements
|Inherited=Yes
|Media=interactive
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Initial value. Indicates the element inherits its '''-ms-overflow-style''' from its parent element. 

In Internet Explorer for the desktop, on the root element, '''auto''' behaves like '''scrollbar'''.

In Internet Explorer, on the root element, '''auto''' behaves like '''-ms-autohiding-scrollbar'''.
}}{{CSS Property Value
|Data Type=none
|Description=Indicates the element does not display scrollbars or panning indicators, even when its content overflows. 

Unlike [[css/properties/overflow|'''overflow''']]: '''hidden''', elements with '''-ms-overflow-style''': '''none''' can still be scrolled via touch panning, keyboard, or mouse wheel.
}}{{CSS Property Value
|Data Type=scrollbar
|Description=Indicates the element displays a classic scrollbar-type control when its content overflows.  

Unlike '''-ms-autohiding-scrollbar''', scrollbars on elements with the  '''-ms-overflow-style''' property set to '''scrollbar'''  always appear on the screen and do not fade out when the element is inactive.

Scrollbars do not overlay content, and therefore take up extra layout space along the edges of the element where they appear.
}}{{CSS Property Value
|Data Type=-ms-autohiding-scrollbar
|Description=Indicates the element displays auto-hiding scrollbars during mouse interactions and panning indicators during touch and keyboard interactions.

Auto-hiding scrollbars overlay content, and therefore do not require extra layout space.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''-ms-overflow-style''' property only has an effect on elements that overflow using the [[css/properties/overflow|'''overflow''']] property.
When using auto-hiding scrollbars, you should ensure your content has sufficient padding to prevent interactive content from being obscured beneath the scrollbar.
|Import_Notes====Syntax===
<code>'''-ms-overflow-style: '''auto '''{{!}}''' none '''{{!}}''' scrollbar '''{{!}}''' -ms-autohiding-scrollbar</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Touch
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}