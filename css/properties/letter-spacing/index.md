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
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. Default spacing.}}
{{CSS_Property_Value|Data Type=length |Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=inherit |Description=}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''letter-spacing''' attribute and the '''letter-spacing''' property to change the space between letters.

This example uses '''blockquote''' as a selector to change the spacing to -0.2 millimeters for all '''blockquote''' objects on the page.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/letter-spacing.htm
|Code=
&lt;STYLE&gt;
    BLOCKQUOTE { letter-spacing:-0.2mm }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the spacing to 1 millimeter when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/letterSpacing.htm
|Code=
&lt;DIV STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.letterSpacing{{=}}'1mm'"&gt;
:
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When specified as a positive '''length''' value, the '''letter-spacing''' attribute adds the specified value to the default spacing between characters within an element. A negative '''length''' value decreases the space between characters. Letter spacing can be influenced by justification.
|Import_Notes=
===Syntax===
<code>'''letter-spacing: '''normal '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}