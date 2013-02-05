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
|Description=The default value; you will be able to see the elements behind the element in question showing through it.
}}{{CSS Property Value
|Data Type=color
|Description=<code>background-color</code> accepts a single color as its value, which can be a keyword, hex, RGB, RGBa, HSL or HSLa color value. See the [[css/value/color|CSS color values]] page for more details.
}}{{CSS Property Value
|Data Type=inherit
|Description=The element's background-color is inherited from its parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The HTML for this example is a series of simple div elements. Each one has the color information applied to it written inside it for ease of reference.
|Code=&lt;h2&gt;Keywords&lt;/h2&gt;
  
&lt;div id="c1"&gt;
  &lt;p&gt;&lt;code&gt;background-color: red;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
&lt;div id="c2"&gt;
  &lt;p&gt;&lt;code&gt;background-color: green;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
&lt;div id="c3"&gt;
  &lt;p&gt;&lt;code&gt;background-color: blue;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
&lt;h2&gt;Hex values&lt;/h2&gt;
  
&lt;div id="c4"&gt;
  &lt;p&gt;&lt;code&gt;background-color: #ff0000;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
&lt;div id="c5"&gt;
  &lt;p&gt;&lt;code&gt;background-color: #008000;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
&lt;div id="c6"&gt;
  &lt;p&gt;&lt;code&gt;background-color: #0000ff;&lt;/code&gt;&lt;/p&gt;
&lt;/div&gt;
  
  etc.
}}{{Single Example
|Language=CSS
|Description=The CSS then floats the divs next to one another and gives them the same basic look. After that, each block is given a different color value, to demonstrate how keywords, hex, RGB(a), HSL(a) and opacity affect them.
|Code=html {
  background: url(bg.png);
  font-family: sans-serif;
  font-size: 10px;
}
  
body {
  width: 1024px;
  margin: 0 auto;
}
  
p {
  color: white;
  text-shadow: 0 1px 1px black;
  padding: 10px;
  font-size: 1.4rem;
}
  
div {
  height: 75px;
  float: left;
  width: 32%;
  margin-right: 1%;
  box-shadow: 0px 0px 10px black;
}
  
h2 {
  clear: both;
  padding-top: 1.5rem;
}
  
#c1 {
  background-color: red;
}
  
#c2 {
  background-color: green;
}
  
#c3 {
  background-color: blue;
}
  
#c4 {
  background-color: #ff0000;
}
  
#c5 {
  background-color: #008000;
}
  
#c6 {
  background-color: #0000ff;
}

etc

|LiveURL=http://chrisdavidmills.github.com/simple-background-color/
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