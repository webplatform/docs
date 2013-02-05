{{Page_Title|background-color}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|<code>background-color</code> allows you to set a color to fill up the background of an element it is applied to. This background color can use any type of CSS color values, from keywords and hex values, to RGB(a) and HSL(a).}}
{{CSS Property
|Initial value=transparent
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=If the color you are setting is a solid color, the computed value will be the hex equivalent of whatever you set. If it is a translucent color, then the computed value will be the RGBa equivalent of whatever you set.
|Animatable=Yes
|CSS object model property=backgroundColor
|Values={{CSS Property Value
|Data Type=transparent
|Description=Default. Color of the next parent object through which the background is visible.
}}{{CSS Property Value
|Data Type=color
|Description=Any color value, including those specified in the Color Table.
}}{{CSS Property Value
|Data Type=inherit
|Description=Color is inherited from the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''background-color''' attribute and the '''background-color''' property to specify the background color.

This example uses an inline style sheet to set the background color to <code>lime</code>.
|Code=&lt;span style{{=}}"font-size: 14px; background-color: lime"&gt;The background color of the text has been set inline using the &lt;b&gt;background-color&lt;/b&gt; attribute.&lt;/span&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-color.htm
}}{{Single Example
|Language=CSS
|Code=exampleOne {
    background-color: teal;
    color: white;
}
 
.exampleTwo {
    background-color: rgb(153,102,153);
    color: rgb(255,255,204);
}
 
.exampleThree {
    background-color: #777799;
    color: #FFFFFF;
}
}}
}}
{{Notes_Section
|Usage=*background-color: named-color

*background-color: rgb value;
 
*background-color: #hex value
|Notes====Remarks===
This property can be set with the other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
Microsoft Internet Explorer 3.0 supports the '''background-color''' attribute, but only when it's set by using the [[css/cssom/properties/background|'''background''']] attribute.
In Windows CE, specifying a value for the '''background-color''' property of the '''OPTION''' element when applied through the [[css/cssom/style|'''style''']] object has no effect.
|Import_Notes====Syntax===
<code>'''background-color: '''''
&lt;color&gt;
'' '''{{!}}''' transparent</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/background-color
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}