{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Font is normal.
}}{{CSS Property Value
|Data Type=italic
|Description=Font is italic.
}}{{CSS Property Value
|Data Type=oblique
|Description=Font is italic.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use '''hn''' as a selector to set the font style to '''italic''' in H3 headings.
|Code=&lt;STYLE&gt;
    H3 { font-style:italic }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-style.htm
}}{{Single Example
|Description=The following example shows how to use inline scripting to set the font style to '''italic''' when an [[dom/events/mousedown|'''onmousedown''']] event occurs.
|Code=&lt;DIV onmousedown{{=}}"this.style.fontStyle{{=}}'italic'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontStyle.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''oblique''' value is available as of Microsoft Internet Explorer 4.0. Internet Explorer 4.0 renders italic and oblique identically.
While, Windows Internet Explorer is shipped with a default '''font-style''', this default can be changed by accessing Internet Options.
|Import_Notes====Syntax===
<code>'''font-style: '''normal '''{{!}}''' italic '''{{!}}''' oblique</code>
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
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}