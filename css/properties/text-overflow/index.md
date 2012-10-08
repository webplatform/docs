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
|Data Type=ellipsis
|Description=Display ellipses (...) for text overflow.
}}{{CSS Property Value
|Data Type=clip
|Description=Default. Simply clip the content and do not display ellipses for text overflow.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use both '''ellipsis''' and '''clip''' values for the '''-ms-text-overflow''' property.  It also demonstrates how the effect of '''-ms-text-overflow''' can be canceled out by setting the [[css/properties/overflow|'''overflow''']] to ''visible''.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;

&lt;head&gt;
&lt;title&gt;text-overflow Attribute Sample&lt;/title&gt;
&lt;style type{{=}}"text/css"&gt;
div.boxed {
	width: 200px;
	height: 1.5em;
	border: 1px solid blue;
	font: 14px Times New Roman, serif;
}
p.caption {
	font-size: x-small;
	margin: 2px 0 40px;
}
&lt;/style&gt;
&lt;/head&gt;

&lt;body&gt;

&lt;div&gt;
  &lt;h1&gt;text-overflow Attribute Sample&lt;/h1&gt;
  &lt;p&gt;Each box (div element) below contains the following text:&lt;/p&gt;
  &lt;div style{{=}}"margin: .5em 0; padding: 5px; background-color: #eee;"&gt;
    We hold these truths to be self-evident, that all people are created equal.&lt;/div&gt;
  &lt;p&gt;Note how the STYLE settings affect the rendering of the text.&lt;/p&gt;
  &lt;div style{{=}}"padding: 4em 2em; border: 1px solid black;"&gt;
    &lt;div id{{=}}"box1" class{{=}}"boxed" style{{=}}"white-space: nowrap; overflow: hidden; text-overflow: clip;"&gt;
      We hold these truths to be self-evident, that all people are created equal.
    &lt;/div&gt;
    &lt;p class{{=}}"caption"&gt;
    &lt;script type{{=}}"javascript"&gt;document.write('STYLE{{=}}"' + document.getElementById('box1').style.cssText + '"');&lt;/script&gt;
    &lt;/p&gt;
    &lt;div id{{=}}"box2" class{{=}}"boxed" style{{=}}"white-space: nowrap; overflow: hidden; text-overflow: ellipsis;"&gt;
      We hold these truths to be self-evident, that all people are created equal.
    &lt;/div&gt;
    &lt;p class{{=}}"caption"&gt;
    &lt;script type{{=}}"javascript"&gt;document.write('STYLE{{=}}"' + document.getElementById('box2').style.cssText + '"');&lt;/script&gt;
    &lt;/p&gt;
    &lt;div id{{=}}"box3" class{{=}}"boxed" style{{=}}"white-space: nowrap; overflow: visible; text-overflow: ellipsis"&gt;
      We hold these truths to be self-evident, that all people are created equal.
    &lt;/div&gt;
    &lt;p class{{=}}"caption"&gt;
    &lt;script type{{=}}"javascript"&gt;document.write('STYLE{{=}}"' + document.getElementById('box3').style.cssText + '"');&lt;/script&gt;
    &lt;/p&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/css/textOverflow.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-text-overflow''' attribute is an extension to CSS, and can be used as a synonym for '''text-overflow''' in IE8 Standards mode.
The '''-ms-text-overflow''' property was introduced in Microsoft Internet Explorer 6
This property only applies to text overflow in the inline direction (horizontal, in normal Western text).  Inline overflow occurs when the text in a line overflows the available width without a breaking opportunity. To force overflow to occur and ellipses to be applied, the author must apply the ''nowrap'' value to the [[css/properties/white-space|'''white-space''']] property on the element, or wrap the content in a &lt;NOBR&gt; tag. If there is no breaking opportunity (for example, the width is narrow or there is a long word that does not break well), then overflow may occur without ''nowrap'' being applied.
This property on the element must be set to something other than ''visible'', the default, in order for ellipses to be rendered.  The best choice is to set [[css/properties/overflow|'''overflow''']] to  ''hidden''.  Setting '''overflow''' to ''scroll'' or ''auto'' will also work, but will show scrollbars.
The hidden text can be selected by selecting the ellipses. When selected, the ellipses will disappear and be replaced by the text to the extent of the layout area.
This property offers an efficient alternative to building ellipses in Dynamic HTML (DHTML). As ellipses may be rendered many times on a single page, using this property can significantly speed up performance.
|Import_Notes====Syntax===
<code>'''-ms-text-overflow: '''ellipsis '''{{!}}''' clip</code>
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