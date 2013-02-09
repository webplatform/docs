{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The text-overflow CSS property determines how overflowed content that is not displayed is signaled to the users. It can be clipped, display an ellipsis ('…', U+2026 HORIZONTAL ELLIPSIS) or a Web author-defined string.}}
{{CSS Property
|Initial value=not defined for shorthand properties
|Applies to=block-level and inline-block elements
|Inherited=No
|Media=visual
|Computed value=see individual properties
|Animatable=No
|CSS object model property=<'text-overflow-mode'> || <'text-overflow-ellipsis'>
|Values={{CSS Property Value
|Data Type=clip
|Description=Default. Simply clips the content and does not display ellipsis for text-overflow.
}}{{CSS Property Value
|Data Type=ellipsis
|Description=Display ellipsis (...) for text overflow after the last letter that entirely fits into a line.
}}{{CSS Property Value
|Data Type=ellipsis-word
|Description=Display ellipsis (...) for text overflow after the last word that entirely fits into a line.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use both '''ellipsis''' and '''clip''' values for the '''text-overflow''' property. It also demonstrates how the effect of '''text-overflow''' can be canceled out by setting the [[css/properties/overflow|'''overflow''']] to ''visible''.
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
}}{{Single Example
|Language=CSS
|Code=p {
  white-space: nowrap;
  width: 100%;                   
  overflow: hidden;        /* "overflow" value must be different from "visible" */
 
  text-overflow:    ellipsis;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
This property only applies to text overflow in the inline direction (horizontal, in normal Western text).  Inline overflow occurs when the text in a line overflows the available width without a breaking opportunity. To force overflow to occur and ellipses to be applied, the author must apply the ''nowrap'' value to the [[css/properties/white-space|'''white-space''']] property on the element, or wrap the content in a &lt;NOBR&gt; tag. If there is no breaking opportunity (for example, the width is narrow or there is a long word that does not break well), then overflow may occur without ''nowrap'' being applied.
This property on the element must be set to something other than ''visible'', the default, in order for ellipses to be rendered.  The best choice is to set [[css/properties/overflow|'''overflow''']] to  ''hidden''.  Setting '''overflow''' to ''scroll'' or ''auto'' will also work, but will show scrollbars.
The hidden text can be selected by selecting the ellipses. When selected, the ellipses will disappear and be replaced by the text to the extent of the layout area.
This property offers an efficient alternative to building ellipses in Dynamic HTML (DHTML). As ellipses may be rendered many times on a single page, using this property can significantly speed up performance.
|Import_Notes====Syntax===
<code>'''text-overflow: '''ellipsis '''{{!}}''' clip</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=7.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.0
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=9.0
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.1
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=10.0
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Yes
|Opera_mini_prefixed_version=5.0-7.0
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
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
|Sources=MDN, MSDN
|MDN_link=http://dev.w3.org/csswg/css3-ui/#text-overflow
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}