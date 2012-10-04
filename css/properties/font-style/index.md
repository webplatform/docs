{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. Font is normal.}}
{{CSS_Property_Value|Data Type=italic |Description=Font is italic.}}
{{CSS_Property_Value|Data Type=oblique |Description=Font is italic.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use '''hn''' as a selector to set the font style to '''italic''' in H3 headings.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-style.htm
|Code=
&lt;STYLE&gt;
    H3 { font-style:italic }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=The following example shows how to use inline scripting to set the font style to '''italic''' when an [[dom/events/mousedown|'''onmousedown''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontStyle.htm
|Code=
&lt;DIV onmousedown{{=}}"this.style.fontStyle{{=}}'italic'"&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''oblique''' value is available as of Microsoft Internet Explorer 4.0. Internet Explorer 4.0 renders italic and oblique identically.
While, Windows Internet Explorer is shipped with a default '''font-style''', this default can be changed by accessing Internet Options.
|Import_Notes=
===Syntax===
<code>'''font-style: '''normal '''{{!}}''' italic '''{{!}}''' oblique</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}