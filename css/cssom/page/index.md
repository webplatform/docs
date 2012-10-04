{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Although '''page''' objects are represented in the Cascading Style Sheets (CSS) object model starting in Microsoft Internet Explorer 5.5,  the objects are not used by the default print template for Windows Internet Explorer.  The objects can be represented explicitly in print templates developed for applications that host MSHTML.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''page''' object has these types of members:
*[#properties Properties]


====Properties====
The '''page''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/cssom/styleSheet/cssText|'''cssText''']]
|Sets or retrieves the persisted representation of the style rule.
|-
|[[css/cssom/CSSRule/parentRule|'''parentRule''']]
|Retrieves the containing rule, if the current rule is contained inside another rule.
|-
|[[css/cssom/CSSRule/parentStyleSheet|'''parentStyleSheet''']]
|Retrieves the style sheet that contains the current rule.
|-
|[[css/cssom/properties/pseudoClass|'''pseudoClass''']]
|Retrieves a string that identifies the pseudo class of the page or pages an '''@page''' rule applies to.
|-
|[[css/cssom/properties/selector|'''selector''']]
|Retrieves a string that identifies which page or pages an '''@page''' rule applies to.
|-
|[[css/cssom/properties/selectorText|'''selectorText''']]
|Sets or retrieves a value that represents the textual representation of the selector for the rule set.
|-
|'''style'''
|Retrieves the declaration block of the current rule.
|-
|[[css/cssom/CSSRule/type|'''type''']]
|Retrieves the type of the rule.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Print Template Reference</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}