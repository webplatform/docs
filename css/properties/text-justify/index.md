{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property changes the justification of each line of text. Changes are made for spacing between letters and words. Applies to both block and inline elements.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Allows the browser to determine which justification algorithm to apply.
}}{{CSS Property Value
|Data Type=distribute
|Description=Handles spacing much like the '''newspaper''' value. This form of justification is optimized for documents in Asian languages, such as Thai.
}}{{CSS Property Value
|Data Type=distribute-all-lines
|Description=Justifies lines of text in the same way as the '''distribute''' value, except that it also justifies the last line of the paragraph. This form of justification is intended for ideographic text.
}}{{CSS Property Value
|Data Type=distribute-center-last
|Description=Not implemented.
}}{{CSS Property Value
|Data Type=inter-cluster
|Description=Justifies lines of text that contain no inter-word spacing. This form of justification is optimized for documents in Asian languages.
}}{{CSS Property Value
|Data Type=inter-ideograph
|Description=Justifies lines of ideographic text, and increases or decreases both inter-ideograph and inter-word spacing.
}}{{CSS Property Value
|Data Type=inter-word
|Description=Aligns text by increasing the space between words. This value's spacing behavior is the fastest way to make all lines of text equal in length. Its justification behavior does not affect the last line of the paragraph.
}}{{CSS Property Value
|Data Type=kashida
|Description=Justifies lines of text by elongating characters at chosen points.  This form of justification is intended for Arabic script languages. Supported starting in Internet Explorer 5.5.
}}{{CSS Property Value
|Data Type=newspaper
|Description=Increases or decreases the spacing between letters and between words. It is the most sophisticated form of justification for Latin alphabets.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''-ms-text-justify''' attribute and the '''-ms-text-justify''' property to align text within the object.

This example uses an inline style sheet to distribute all the lines within the object.
|Code=...
&lt;DIV style{{=}}"text-align:justify; text-justify:distribute-all-lines;"&gt;
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
    This is something. This example demonstrates how to this 
    property. This is something. This example demonstrates how to use this
    property. This is something. This example demonstrates how to
    use this property. This is something. This example demonstrates
    how to use this property. This is something. This example
    demonstrates how to use this property. This is something.
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
&lt;/DIV&gt;                
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-justify.htm
}}{{Single Example
|Description=This example uses inline scripting to change the alignment of the text when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=...
&lt;DIV style{{=}}"cursor:hand; text-align:justify;"
    onmouseover{{=}}"this.style.textJustify{{=}}'distribute-all-lines';"
    onmouseout{{=}}"this.style.textJustify{{=}}'auto';"&gt;
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
    This is something. This example demonstrates how to this 
    property. This is something. This example demonstrates how to use this
    property. This is something. This example demonstrates how to
    use this property. This is something. This example demonstrates
    how to use this property. This is something. This example
    demonstrates how to use this property. This is something.
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
&lt;/DIV&gt;                
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textJustify.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-text-justify''' attribute is an extension to CSS, and can be used as a synonym for '''text-justify''' in IE8 Standards mode.
For this property to affect text layout, the [[css/properties/text-align|'''text-align''']] property must be set to '''justify'''.
The property applies to block elements.
|Import_Notes====Syntax===
<code>'''-ms-text-justify: '''auto '''{{!}}''' distribute '''{{!}}''' distribute-all-lines '''{{!}}''' distribute-center-last '''{{!}}''' inter-cluster '''{{!}}''' inter-ideograph '''{{!}}''' inter-word '''{{!}}''' kashida '''{{!}}''' newspaper</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 8.3
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