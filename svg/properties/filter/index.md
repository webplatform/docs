{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
[[svg/elements/filter|'''Filter''']] elements are never rendered directly; their only usage is as something that can be referenced using the '''filter''' property. Be aware that '''filter''' elements are available for referencing even when the [[css/properties/display|'''display''']] property on the '''filter''' element or any of its ancestors is set to '''none'''.
In the following example, a previously defined Gaussian_Blur filter (that is, <code>filter:url(#Gaussian_Blur)"/&gt;</code>) is being applied to an SVG ellipse:
 <code>&lt;ellipse cx{{=}}"200" cy{{=}}"150" rx{{=}}"70" ry{{=}}"40"
          style{{=}}"fill:#ff0000; stroke:#000000;
          stroke-width:2; filter:url(#Gaussian_Blur)"/&gt;</code>
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[svg/elements/filter|Filter]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}