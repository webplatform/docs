{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the maximum [[css/properties/height|height]] for an element. It prevents the height of the element to exceed the specified value. If [[css/properties/min-height|min-height]] is specified and is greater than max-height, max-height is overridden.}}
{{CSS Property
|Initial value=none
|Applies to=All elements but non-replaced inline elements, table columns, and column groups
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length or 'none'
|Animatable=Yes
|CSS object model property=max-height
|CSS percentages=refer to height of containing block
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed height. Negative values are not allowed. See [[css/units/length|length]] for possible units.
}}{{CSS Property Value
|Data Type=percentage
|Description=A <percentage> relative to the height of the containing block. If the containing block has no height explicitly set then is is treated as none. Negative values are not allowed.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}{{CSS Property Value
|Data Type=none
|Description=Clears the max-height value. The height property can have any value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows a div element with and without a max height property applied.
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
|Import_Notes====Standards information===
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