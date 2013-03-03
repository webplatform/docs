{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the minimum [[css/properties/height|height]] for an element. It prevents the height of the element to exceed the specified value.
It overrides both the height & the max-height property if any them is specified below the min-height value.
}}
{{CSS Property
|Initial value=auto (0 for non-flex elements)
|Applies to=All elements but non-replaced inline elements, table columns, and column groups
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length
|Animatable=Yes
|CSS object model property=min-height
|CSS percentages=Of the height of containing block. If the height of the containing block depends on the content & the element does not have position as absolute, then this value becomes 0.
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed height. Negative values are not allowed. See [[css/units/length|length]] for possible units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A <percentage> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as 0. Negative values are not allowed
}}{{CSS Property Value
|Data Type=calc()
|Description=See [[css/functions/calc|css calc function]] for mode details.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following Internet Explorer 6 example shows the benefits of using the '''min-height''' attribute over the [[html/attributes/height|'''HEIGHT''']] attribute for a '''tr''' element.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;title&gt;min-height Attribute Example&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;table border{{=}}"1" style{{=}}"table-layout: fixed; width: 100%;"&gt;
    &lt;tr&gt;
        &lt;td style{{=}}"height: 35px; background-color: #99CCFF"&gt;This cell has the &lt;b&gt;
        height&lt;/b&gt; attribute set to 35px. In Internet Explorer, overflow text is 
        clipped when &lt;b&gt;height&lt;/b&gt; is set on cells or rows in fixed-layout tables. 
        Setting the &lt;b&gt;min-height&lt;/b&gt; attribute, however, accommodates overflow text 
        by increasing the cell or row height.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td style{{=}}"min-height: 35px; background-color: #99CCFF"&gt;This cell has the
        &lt;b&gt;min-height&lt;/b&gt; attribute set to 35px. In Internet Explorer, overflow 
        text is clipped when &lt;b&gt;height&lt;/b&gt; is set on cells or rows in fixed-layout 
        tables. Setting the &lt;b&gt;min-height&lt;/b&gt; attribute, however, accommodates overflow 
        text by increasing the cell or row height.&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/minheight.htm
}}{{Single Example
|Description=The following Internet Explorer 7 example shows how the '''min-height''' and [[css/properties/max-height|'''max-height''']] attributes affect the layout of a '''div''' element. Internet Explorer 7 is required to view the example.
|Code=&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
.height {
    float: left;
    width: 300px;
    background: #fff;
    margin: 0 1em;
}
#example1 {
    min-height: 200px;
}
#example2 {
    max-height: 100px;
}
.content {
    border: 1px solid #c00;
    padding: 5px;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class{{=}}"height" id{{=}}"example1"&gt;
    &lt;div class{{=}}"content"&gt;
        &lt;h2&gt;{ min-height:200px }&lt;/h2&gt;
        &lt;p&gt;The height of this div is always at least 200px.&lt;br /&gt;
        &lt;br /&gt;
        The content does not fill the entire div.&lt;/p&gt;
    &lt;/div&gt;
&lt;/div&gt;
&lt;div class{{=}}"height" id{{=}}"example2"&gt;
    &lt;div class{{=}}"content"&gt;
        &lt;h2&gt;{ max-height:100px }&lt;/h2&gt;
        &lt;p&gt;This div will not grow more than 100px in height.&lt;br /&gt;
        &lt;br /&gt;
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
In Internet Explorer 6, this property applies only to '''td''', '''th''', and '''tr''' elements in fixed-layout tables. To create a fixed-layout table, set the [[css/properties/table-layout|'''table-layout''']] property of a [[html/elements/table|'''table''']] element to <code>fixed</code>. The advantage of a fixed-layout table is that it renders faster than an auto-layout table. Auto-layout tables are the default.
In Internet Explorer 7, the '''min-height'''/[[css/properties/max-height|'''max-height''']] attributes apply to floating and absolutely positioned block, inline-block elements, and some intrinsic controls. They do not apply to non-replaced inline elements, such as table columns and row/column groups. (A "replaced" element has intrinsic dimensions, such as an '''img''' or '''textArea'''.)
In Internet Explorer 7, this property is enabled only under the strict [[html/elements/!DOCTYPE|!DOCTYPE]].
|Import_Notes====Syntax===
<code>'''min-height: '''''
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
*<code>Reference</code>
*<code>[[html/attributes/height|height]]</code>
*<code>Other Resources</code>
*<code>Cascading Style Sheet Compatibility in Internet Explorer 7</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}