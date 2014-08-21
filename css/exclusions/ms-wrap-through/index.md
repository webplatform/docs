{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Broswer bias. Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/exclusions
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
You can use the '''-ms-wrap-through''' property to control the effect of exclusions—for instance, to cause one content block to wrap around an exclusion element and another to intersect the same exclusion element.
The ''wrapping context'' of a box is a collection of exclusion areas contributed by its associated exclusion boxes. When Windows Internet Explorer lays out a webpage, a box wraps its inline flow content in the area that corresponds to the subtraction of its wrapping context from its own content area. For more information about exclusion elements' impact on content flow, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}234931 Definitions] section of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}234148 CSS3 Exclusions] specification.
|Import_Notes====Syntax===
<code>'''-ms-wrap-through: '''wrap '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkId{{=}}234148 CSS Exclusions and Shapes Module Level 3], Section 3.3.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Exclusions
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}236927 Internet Explorer 10 Guide for Developers: CSS Exclusions]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}