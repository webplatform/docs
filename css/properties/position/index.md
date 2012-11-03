{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Perhaps one of the hardest properties fully master, the position property controls the type of positioning used by an element within its parent elements. The effect of the position attribute depends on a lot of factors including the positioning type of parent elements.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=static
|Description=Default. Object has no special positioning; it follows the layout rules of HTML.
}}{{CSS Property Value
|Data Type=absolute
|Description=Object is positioned relative to parent element's position—or to the '''body''' object if its parent element is not positioned—using the [[css/properties/top|'''top''']] and [[css/properties/left|'''left''']] properties.
}}{{CSS Property Value
|Data Type=relative
|Description=Object is positioned according to the normal flow, and then offset by the [[css/properties/top|'''top''']] and [[css/properties/left|'''left''']] properties.
}}{{CSS Property Value
|Data Type=fixed
|Description=Starting in Internet Explorer 7. Object is positioned relative to the viewport containing the content.
}}{{CSS Property Value
|Data Type=sticky
|Description=The lovechild of "static" and "fixed", an object with this value behaves as relative until a threshold defined by a top/bottom/left/right property is crossed, at which point it behaves as position: fixed within its positioned parent container.
}}{{CSS Property Value
|Data Type=page
|Description=Internet Explorer 10. Positioned floats only. (The [[css/properties/display|'''display''']] property must be set to '''-ms-positioned'''.) Object is positioned relative to the nearest [http://go.microsoft.com/fwlink/p/?LinkId{{=}}226824 initial containing block]. This may be the browser or application window or a content container such as an '''iframe'''. The [[css/properties/bottom|'''bottom''']], [[css/properties/top|'''top''']], [[css/properties/left|'''left''']], and [[css/properties/right|'''right''']] properties are used to position the element relative to the boundaries of the viewport that the positioned float would normally be placed in (that is, if '''position:static''' was set). For more information, see Positioned Floats.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This examples uses the '''position''' property's '''absolute''', '''static''', and '''relative''' values to change the position of the text.
|Code=&lt;style type{{=}}"text/css"&gt;
.pitem {
	position: static;
}
&lt;/style&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnAbsolute(){
   oSpan.style.position{{=}}"absolute";
}
function fnRelative(){
   oSpan.style.position{{=}}"relative";
}
function fnStatic(){
   oSpan.style.position{{=}}"static";
}
&lt;/script&gt;
&lt;p&gt;&lt;span id{{=}}"oSpan" class{{=}}"pitem"&gt;This is a &lt;b&gt;span&lt;/b&gt; in a paragraph of text.&lt;/span&gt; 
This is a paragraph of text.&lt;/p&gt;
&lt;input onclick{{=}}"fnRelative()" type{{=}}"button" value{{=}}"Relative"&gt;
&lt;input onclick{{=}}"fnAbsolute()" type{{=}}"button" value{{=}}"Absolute"&gt;
&lt;input onclick{{=}}"fnStatic()" type{{=}}"button" value{{=}}"Static"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/position.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Setting the property to '''absolute''' pulls the object out of the "flow" of the document and positions it regardless of the layout of surrounding objects. If other objects already occupy the given position, they do not affect the positioned object, nor does the positioned object affect them. Instead, all objects are drawn at the same place, causing the objects to overlap. This overlap is controlled by using the [[css/properties/z-index|'''z-index''']] attribute or property. Absolutely positioned objects do not have margins, but they do have borders and padding.
To enable absolute positioning on an object you must specify at least one of the [[css/properties/top|'''top''']], [[css/properties/bottom|'''bottom''']], [[css/properties/left|'''left''']], or [[css/properties/right|'''right''']] properties, in addition to setting the '''position''' property to '''absolute'''. Otherwise, these positioning properties use their default value of '''absolute''', which causes the object to render immediately after the preceding elements, according to the layout rules of HTML
Input from pointing devices, such as the mouse, does not penetrate through overlapping elements even if the elements are not visible. This is also true for positioned elements with a negative z-index unless:
*The parent is a scrolling container (that is, its [[css/properties/overflow|'''overflow''']] property is set to '''auto''' or '''scroll''').
*The parent is positioned (that is, its '''position''' property is set to '''absolute''' or '''relative''').

Setting the property to '''relative''' places the object in the natural HTML flow of the document, but offsets the position of the object based on the preceding content. The following syntax shows how to create superscript text by placing the text in a '''span''' that is positioned relative to the remaining text in the paragraph.
 <code>&lt;p&gt;The superscript in this name 
     &lt;span style{{=}}"position: relative; 
     top: -3px"&gt;xyz&lt;/span&gt; is &amp;quot;xyz&amp;quot;.&lt;/p&gt;</code>
Text and objects that follow a relatively positioned object occupy their own space and do not overlap the natural space for the positioned object. In contrast, text and objects that follow an absolutely positioned object occupy what would have been the natural space for the positioned object before it was pulled out of the flow. Placing an absolutely positioned object beyond the viewable area of the window causes a scroll bar to appear. When relatively positioned objects are placed beyond the viewable area, a scroll bar is not shown.
The size of the content determines the size of objects with layout. For example, setting the [[css/properties/height|'''height''']] and '''position''' properties on a '''div''' object gives it layout. The content of the '''div''' determines the size. In this case, the content determines the size of the [[css/properties/width|'''width''']].
Starting in Internet Explorer 7. Fixed positioning is only supported for pages using a strict [[dom/properties/doctype|'''&lt;!DOCTYPE&gt; directive''']].
For an overview about how to use dynamic positioning, see About Element Positioning.
Internet Explorer 10. Setting the '''position''' property to '''page''' requires that the [[css/properties/display|'''display''']] property be set to '''-ms-positioned'''. Furthermore, setting '''display''' to '''-ms-positioned''' makes the other values for the '''position''' property behave in the following ways:
*'''static'''  Default. The positioned float is laid out according to normal HTML flow.
*'''absolute'''  The positioned float is laid out relative to its containing block, but the positioned float will affect the normal flow of its container. Inline content wraps around the positioned float; the positioned float is not laid out on top of inline content.
*'''relative'''  The positioned float is laid out relative to where it would fall in the normal flow. The [[css/properties/bottom|'''bottom''']], [[css/properties/top|'''top''']], [[css/properties/left|'''left''']], and [[css/properties/right|'''right''']] properties can be used to calculate an offset from the element's position in the normal flow. Content will flow around the original position of the element, and the actual positioned float will be superimposed on top of inline content.
*'''fixed'''  The positioned float is laid out relative to the initial position of the viewport, or browser window. (The positioned float's position is not updated as the viewport moves due to scrolling.)

For more information, see Positioned Floats.
|Import_Notes====Syntax===
<code>'''position: '''static '''{{!}}''' relative '''{{!}}''' absolute '''{{!}}''' fixed '''{{!}}''' page</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.3.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=position: sticky
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=Canary 23.0.1247.0+ (with flag enabled)
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=Nightlies
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
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