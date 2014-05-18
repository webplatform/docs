{{Page_Title|font-variant}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Selects a normal, or small-caps face from a font family. Also possible by using the font shorthand.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=yes
|Media=visual
|Computed value=As specified
|Animatable=no
|CSS object model property=N/A
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Specifies a normal font face.
}}{{CSS Property Value
|Data Type=small-caps
|Description=Specifies a small-caps labeled font. If no small-case font is available, some browser (e.g. Firefox) simulate a small-case font by replacing the lowercase characters by scaled uppercase letters.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherit to the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the '''font-variant''' attribute and the '''font-variant''' property to change the font to small capitals.
|Code=&lt;P STYLE{{=}}"font-variant:small-caps"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-variant.htm
}}{{Single Example
|Language=CSS
|Description=This example uses inline scripting to set the font style to '''small-caps''' when an [[dom/events/mousedown|'''onmousedown''']] event occurs.
|Code=&lt;DIV onmousedown{{=}}"this.style.fontVariant{{=}}'small-caps'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontVariant.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Microsoft Internet Explorer 4.0 renders '''small-caps''' as uppercase letters in a smaller size.
|Import_Notes====Syntax===
<code>'''font-variant: '''normal '''{{!}}''' small-caps</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 3
|URL=http://www.w3.org/TR/css3-fonts/#font-variant-prop
|Status=W3C Candidate Recommendation
|Relevant_changes=Extends the property (not yet in this entry)
}}{{Related Specification
|Name=CSS
|URL=http://www.w3.org/TR/CSS1/#font-variant
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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
{{Topics|CSS, Design}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}