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
|Language=CSS
|Code=/* Restrict all div elements to a max-height of 10px */
div { max-height: 10px }
}}{{Single Example
|Language=HTML
|Description=Div elements with and without max-height applied (Only the relevant section of the page)
|Code=<style>
/*Default width. Height is based on the content*/
.without-max-height, .with-max-height {
    width: 100px;
}

/*Max height overrides height*/
.with-max-height {
    background: cyan;
    max-height: 50px;
}

.without-max-height {
	background: red;
}
</style>
<div class="without-max-height">Without Max Height. Height taken from content</div>
<br>
<div class="with-max-height">With Max Height. Content may overflow if it goes beyond height.</div>
<br>
|LiveURL=http://code.webplatform.org/gist/5070850
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