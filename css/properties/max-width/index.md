{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=length |Description=Floating-point number followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.}}
{{CSS_Property_Value|Data Type=percentage |Description=Integer followed by a % that specifies a percentage of the containing block width to use as the maximum width of the element.  If the width of the containing block is not explicitly set, then the element has no maximum width and the  '''max-width''' property is interpreted as 0%. For more information on containing blocks and how their widths are computed, see the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203760 Cascading Style Sheets, Level 2.1 (CSS2.1)] specification.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to constrain the width of a '''div''' element using [[css/properties/min-width|'''min-width''']] and '''max-width''' attributes. The example requires Internet Explorer 7 or later to view.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/minWidth7.htm
|Code=
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style&gt;
.width {
    width:50%;
    min-width:200px;
    max-width:400px;
    background:#eee;
}
.content {
    border:1px solid #c00;
    padding:5px;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class{{=}}"width"&gt;
&lt;div class{{=}}"content"&gt;
        &lt;h2&gt;{ min-width:200px; max-width:400px }&lt;/h2&gt;
        &lt;p&gt;This div also has a width of 50%. Resize the window
         to grow and shrink the div from max to min width.&lt;br/&gt;&lt;br/&gt;
         The outer div controls the width of the inner "content" div.
         Note that the div height increases to accommodate the flow of text.&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''max-width''' was introduced in Windows Internet Explorer 7.
The [[css/properties/min-width|'''min-width''']]/'''max-width''' attributes apply to floating and absolutely positioned block and inline-block elements, as well as some intrinsic controls. They do not apply to non-replaced inline elements, such as table rows and row/column groups. (A "replaced" element has intrinsic dimensions, such as an '''img''' or '''textArea'''.)
This property is enabled only under the strict [[html/elements/!DOCTYPE|!DOCTYPE]].
|Import_Notes=
===Syntax===
<code>'''max-width: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 10.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Cascading Style Sheet Compatibility in Internet Explorer 7</code>
|Topic_clusters=Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}