{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=transparent
|Description=Border is transparent.
}}{{CSS Property Value
|Data Type=color
|Description=Up to four color names or RGB values in the Color Table.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-color''' attribute and the '''border-color''' property to specify the border color.

This example uses a call to an embedded (global) style sheet to change the color of the border to <code>blue</code> from an initial value of <code>red</code> when the mouse moves over the image.
|Code=&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
TD {
    border-color: red;
    border-width: 0.5cm;
}
.blue {
    border-color: blue;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;table border{{=}}""&gt;
    &lt;tr&gt;
        &lt;td onmouseover{{=}}"this.className{{=}}'blue'" onmouseout{{=}}"this.className{{=}}''"&gt;
        &lt;img alt{{=}}"sphere" src{{=}}"sphere.jpg"&gt; &lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-color.htm
}}{{Single Example
|Description=This example uses inline scripting to change the color of the border to <code>blue</code> when the mouse moves over the image.
|Code=&lt;td onmouseover{{=}}"this.style.borderWidth{{=}}'0.5cm';
                 this.style.borderColor{{=}}'blue';
                 this.style.borderStyle{{=}}'solid'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderColor.htm
}}{{Single Example
|Description=This example uses embedded styles to change the border from a value of <code>transparent</code> to a value of <code>gold</code>.
|Code=&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
a:link, a:visited {
    border-style: solid; 
    border-width: 10px;
    border-color: transparent;
}
a:hover {
    border-style: ridge;
    border-width: 10px;
    border-color: gold;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;a href{{=}}"#"&gt;Yes.&lt;/a&gt;&amp;nbsp;&amp;nbsp;&lt;a href{{=}}"#"&gt;No.&lt;/a&gt;&amp;nbsp;&amp;nbsp;&lt;a href{{=}}"#"&gt;Maybe so.&lt;/a&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-color0.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Up to four different colors can be specified in the following order: top, right, bottom, left. If one color is supplied, it is used for all four sides. If two colors are supplied, the first is used for the top and bottom, and the second is used for left and right. If three colors are supplied, they are used for top, right and left, and bottom, respectively.
The '''border-color''' property does not render if the [[css/properties/border-style|'''border-style''']] property is set to '''none'''.
Some browsers do not recognize color names, but all browsers should recognize RGB color values and display them correctly.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
<code>'''border-color: ''''''[''' ''
&lt;color&gt;
'' '''{{!}}''' transparent ''']''''''
{1,4}
'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.16
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
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}