{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Browser bias. Needs summary, spec reference, standardization status 
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
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''-ms-wrap-flow''' property makes an element an exclusion element when it has a computed value other than '''auto'''. This property specifies that the exclusion element (the exclusion) can be positioned in various ways, and that inline content will wrap around the exclusion in a way similar to how it wraps around floated elements.
When the '''-ms-wrap-flow''' property's computed value is '''auto''', the element does not become an exclusion element unless its [[css/properties/float|'''float''']] property's computed value is not '''none'''. In that case, the element contributes its border box to its containing block's wrapping context and content flows around it according to the [[css/properties/clear|'''clear''']] property. For more information about exclusion elements' impact on content flow, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}234931 Definitions] section of the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}234148 CSS3 Exclusions] specification.
|Import_Notes====Syntax===
<code>'''-ms-wrap-flow: '''auto '''{{!}}''' both '''{{!}}''' start '''{{!}}''' end '''{{!}}''' maximum '''{{!}}''' clear</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkId{{=}}234148 CSS Exclusions and Shapes Module Level 3], Section 3.1.1
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
|Manual_links=
|External_links=
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