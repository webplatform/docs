{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Increases or decreases the space between characters in a text.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Default spacing.
}}{{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''letter-spacing''' attribute and the '''letter-spacing''' property to change the space between letters.

This example uses '''blockquote''' as a selector to change the spacing to -0.2 millimeters for all '''blockquote''' objects on the page.
|Code=&lt;STYLE&gt;
    BLOCKQUOTE { letter-spacing:-0.2mm }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/letter-spacing.htm
}}{{Single Example
|Description=This example uses inline scripting to set the spacing to 1 millimeter when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;DIV STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.letterSpacing{{=}}'1mm'"&gt;
:
&lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/letterSpacing.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
When specified as a positive '''length''' value, the '''letter-spacing''' attribute adds the specified value to the default spacing between characters within an element. A negative '''length''' value decreases the space between characters. Letter spacing can be influenced by justification.
|Import_Notes====Syntax===
<code>'''letter-spacing: '''normal '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}