{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px).
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). This value is a percentage of the width of the parent object.
}}{{CSS Property Value
|Data Type=inherit
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''text-indent''' attribute and the '''text-indent''' property to indent the object's text.

This example uses calls to an embedded style sheet to change the indent on the text when an [[dom/events/click|'''onclick''']] event occurs. The text was originally indented 2 centimeters using '''div''' as a selector in the style sheet.
|Code=&lt;STYLE&gt;
    DIV { text-indent:2cm }
    .click1 { text-indent:50% }
    .click2 { text-indent: }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;DIV onclick{{=}}"this.className{{=}}'click1'"
    ondblclick{{=}}"this.className{{=}}'click2'"&gt;
. . . &lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-indent.htm
}}{{Single Example
|Description=This example uses inline scripting to indent the text within the '''div''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;DIV onmouseover{{=}}this.style.textIndent{{=}}"2cm"
:
&lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textIndent.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The property can be negative. An indent is not inserted in the middle of an object that was broken by another object, such as '''br''' in HTML.
|Import_Notes====Syntax===
<code>'''text-indent: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.7
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
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
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