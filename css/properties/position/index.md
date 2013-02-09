{{Page_Title}}
{{Flags
|Content=Not Neutral, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The position property controls the type of positioning used by an element within its parent elements. The effect of the position attribute depends on a lot of factors, for example the value of position property of parent elements.}}
{{CSS Property
|Initial value=static
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=As specified, or none if none given
|Animatable=No
|CSS object model property=position
|Values={{CSS Property Value
|Data Type=static
|Description=Default. Object has no special positioning; it follows the layout rules of HTML. Values of [[css/properties/top|'''top''']], [[css/properties/bottom|"bottom"]], [[css/properties/left|"left"]] and [[css/properties/right|"right"]] have no impact.
}}{{CSS Property Value
|Data Type=absolute
|Description=Object is positioned relative to parent element's position—or to the '''body''' object if its parent element is not positioned—using the [[css/properties/top|'''top''']] and [[css/properties/left|'''left''']] properties.
}}{{CSS Property Value
|Data Type=relative
|Description=Object is positioned according to the normal flow, and then offset by the [[css/properties/top|'''top''']] and [[css/properties/left|'''left''']] properties.
}}{{CSS Property Value
|Data Type=fixed
|Description=Object is positioned relative to the viewport containing the content. Object stays in the viewport when scrolling. Usually used for navigation on mobile devices. Limited support.
}}{{CSS Property Value
|Data Type=sticky
|Description=The lovechild of "static" and "fixed", an object with this value behaves as relative until a threshold defined by a top/bottom/left/right property is crossed, at which point it behaves as position: fixed within its positioned parent container.
}}{{CSS Property Value
|Data Type=page
|Description=Internet Explorer 10. Positioned floats only. (The [[css/properties/display|'''display''']] property must be set to '''-ms-positioned'''.) Object is positioned relative to the nearest [http://go.microsoft.com/fwlink/p/?LinkId{{=}}226824 initial containing block]. This may be the browser or application window or a content container such as an '''iframe'''. The [[css/properties/bottom|'''bottom''']], [[css/properties/top|'''top''']], [[css/properties/left|'''left''']], and [[css/properties/right|'''right''']] properties are used to position the element relative to the boundaries of the viewport that the positioned float would normally be placed in (that is, if '''position:static''' was set). For more information, see Positioned Floats.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the value of the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows the usage of different position values on a child dependent of the position value of its parent.
|Code=&lt;section class="parent static"&gt;
    &lt;div class="child absolute"&gt;
        &lt;p&gt;absolute&lt;/p&gt;
    &lt;/div&gt;
    &lt;p&gt;static&lt;/p&gt;
&lt;/section&gt;

&lt;section class="parent static"&gt;
    &lt;div class="child static"&gt;
        &lt;p&gt;static&lt;/p&gt;
    &lt;/div&gt;
    &lt;p&gt;static&lt;/p&gt;
&lt;/section&gt;
    
&lt;section class="parent static"&gt;
    &lt;div class="child relative"&gt;
        &lt;p&gt;relative&lt;/p&gt;
    &lt;/div&gt;
    &lt;p&gt;static&lt;/p&gt;
&lt;/section&gt;
     
&lt;section class="parent relative"&gt;
    &lt;div class="child absolute"&gt;
        &lt;p&gt;absolute&lt;/p&gt;
    &lt;/div&gt;
    &lt;p&gt;relative&lt;/p&gt;
&lt;/section&gt;
|LiveURL=http://jsfiddle.net/DqxfR/
}}{{Single Example
|Language=CSS
|Description=Watch how the child positions itself within the parent, dependent on the value of position on both elements.
|Code=.static {
    position: static;
}

.relative {
    position: relative;
}

.absolute {
    position: absolute;
}

.fixed {
    position: fixed;    
}

.child {
    top: 30px;
    left: 20px;
    
    background-color: #ff3856;
    width: 100px;
    height: 100px;
}

.parent {
    background-color: #6acc18;
    margin: 80px;
    width: 160px;
    height: 160px;
}
}}
}}
{{Notes_Section
|Usage====Absolute===

Setting the property to absolute pulls the object out of the "flow" of the document and positions it regardless of the layout of surrounding objects. If other objects already occupy the given position, they do not affect the positioned object, nor does the positioned object affect them. Instead, all objects are drawn at the same place, causing the objects to overlap. (This overlap is controlled by using the z-index attribute or property.)

To enable absolute positioning on an object you must specify at least one of the top, bottom, left, or right properties, in addition to setting the position property to absolute. Otherwise, these positioning properties use their default value of absolute, which causes the object to render immediately after the preceding elements, according to the layout rules of HTML.

Absolute positioning behaves differently dependent on the position value of the parent element. If a child element is set to position: absolute it behaves like this: 

* If the parents position is '''static''' or '''default''', the position of the child element is calculated relative to the whole document based on top, bottom, left or right attributes.
* If the parents position is not static ('''relative''', '''absolute''' or '''fixed''') the position of the child is calculated relative to the parent element and based on '''top''', '''bottom''', '''left''' or '''right''' attributes.

Absolutely positioned objects do not have '''margins''', but they do have borders and padding.

====Side Note====
Input from pointing devices, such as the mouse, does not penetrate through overlapping elements even if the elements are not visible. This is also true for positioned elements with a negative z-index unless:

* The parent is a scrolling container (that is, its overflow property is set to auto or scroll). 
* The parent is positioned (that is, its position property is set to absolute or relative).

===Relative===
Setting the property to '''relative''' places the object in the natural HTML flow of the document, but offsets the position of the object based on the preceding content. The following syntax shows how to create superscript text by placing the text in a span that is positioned relative to the remaining text in the paragraph.

<nowiki>
<p>The superscript in this name 
    <span style="position: relative; 
    top: -3px">xyz</span> is &quot;xyz&quot;.</p>
</nowiki>

Text and objects that follow a relatively positioned object occupy their own space and do not overlap the natural space for the positioned object. In contrast, text and objects that follow an absolutely positioned object occupy what would have been the natural space for the positioned object before it was pulled out of the flow. Placing an absolutely positioned object beyond the viewable area of the window causes a scroll bar to appear. When relatively positioned objects are placed beyond the viewable area, a scroll bar is not shown. The size of the content determines the size of objects with layout. For example, setting the height and position properties on a div object gives it layout. The content of the div determines the size. In this case, the content determines the size of the width. 


===Fixed===
An element with a '''fixed''' position is positioned relative to the visible viewport. It does not move away if the browser window is scrolled but appears to be fixed in the viewport. A common pattern and example is to use position: fixed on navigation elements that should be visible on the whole page regardless of the scrollbar position. Fixed positioning is only supported for pages using a strict <!DOCTYPE> directive.

===Short===
static Default. 
The positioned float is laid out according to normal HTML flow.

absolute The positioned float is laid out relative to its containing block, but the positioned float will affect the normal flow of its container. Inline content wraps around the positioned float; the positioned float is not laid out on top of inline content.

relative The positioned float is laid out relative to where it would fall in the normal flow. The bottom, top, left, and right properties can be used to calculate an offset from the element's position in the normal flow. Content will flow around the original position of the element, and the actual positioned float will be superimposed on top of inline content.

fixed The positioned float is laid out relative to the initial position of the viewport, or browser window. (The positioned float's position is not updated as the viewport moves due to scrolling.)


}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=position: static, absolute, relative
|Chrome_supported=Yes
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
|Opera_version=4.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=position: fixed
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
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
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=position: static, absolute, relative
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=position: fixed
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
}}
{{Topics|CSS, Design, UI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}