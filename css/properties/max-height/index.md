{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the maximum height for an element.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Floating-point number followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer followed by a % that specifies a percentage of the containing block height to use as the maximum height of the element.  If the height of the containing block is not explicitly set, then the element has no maximum height and the  '''max-height''' property is interpreted as 0%. For more information on containing blocks and how their heights are computed, see the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203760 Cascading Style Sheets, Level 2.1 (CSS2.1)] specification.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how the [[css/properties/min-height|'''min-height''']] and '''max-height''' attributes affect the layout of a '''div''' element. The example requires Internet Explorer 7 or later to view.
|Code=&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style&gt;
.height {
    float:left;
    width:300px;
    background:#fff;
    margin:0 1em;
}
#example1 { min-height:200px; }
#example2 { max-height:100px; }
.content {
    border:1px solid #c00;
    padding:5px;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class{{=}}"height" id{{=}}"example1"&gt;
&lt;div class{{=}}"content"&gt;
    &lt;h2&gt;{ min-height:200px }&lt;/h2&gt;
    &lt;p&gt;The height of this div is always at least 200px.&lt;br/&gt;&lt;br/&gt;
        The content does not fill the entire div.&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;div class{{=}}"height" id{{=}}"example2"&gt;
&lt;div class{{=}}"content"&gt;
    &lt;h2&gt;{ max-height:100px }&lt;/h2&gt;
    &lt;p&gt;This div will not grow more than 100px in height.&lt;br/&gt;&lt;br/&gt;
        The content that does not fit in the div continues beyond it.&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/minHeight7.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
'''max-height''' was introduced in Windows Internet Explorer 7.
The [[css/properties/min-height|'''min-height''']]/'''max-height''' attributes apply to floating and absolutely positioned block and inline-block elements, as well as some intrinsic controls. They do not apply to non-replaced inline elements, such as table columns and row/column groups. (A "replaced" element has intrinsic dimensions, such as an '''img''' or '''textArea'''.)
This property is enabled only under the strict [[html/elements/!DOCTYPE|!DOCTYPE]].
|Import_Notes====Syntax===
<code>'''max-height: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 10.7
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
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Cascading Style Sheet Compatibility in Internet Explorer 7</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}