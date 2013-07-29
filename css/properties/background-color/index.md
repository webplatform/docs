{{Page_Title|background-color}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets a color to fill up the background of an element it is applied to and accepts any valid CSS color.}}
{{CSS Property
|Initial value=transparent
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=the computed color
|Animatable=Yes
|CSS object model property=backgroundColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=transparent
|Description=The default value; you will be able to see the elements behind the element in question showing through it.
}}{{CSS Property Value
|Data Type=color
|Description=<code>background-color</code> accepts a single color as its value, which can be a keyword, hex, RGB, RGBa, HSL or HSLa color value. See the [[css/color|CSS color values]] page for more details.
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
|Usage=* A strongly contrasting combination of foreground and background color should be used to make sure your textual content is as readable as possible. To check whether your color contrast passes accessibility conformance criteria, you can use an online checker such as [http://leaverou.github.com/contrast-ratio Lea Verou’s Contrast Ratio] which accepts any valid CSS color.
* When using a newer color value type such as RGBa, HSL or HSLa, be aware that older browsers such as IE6-8 don't support these, so you should provide a fallback colour value so that foreground text will still be readable, either in the same stylesheet, or hidden away behind a [http://dev.opera.com/articles/view/supporting-ie-with-conditional-comments/ conditional comment]. So for example:
<pre class="lang-css">
background-color: #ff0000;
background-color: rgba(255,0,0,0.6);
</pre>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds & Borders Level 3
|URL=http://www.w3.org/TR/css3-background/#the-background-color
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=CSS 2.1 Colors and backgrounds
|URL=http://www.w3.org/TR/CSS21/colors.html
|Status=W3C Recommendation
}}
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
}}{{Compatibility Table Desktop Row
|Feature=Opacity
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=RGBa
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=HSL and HSLa
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
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
}}{{Compatibility Table Mobile Row
|Feature=Opacity
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
|Feature=RGBa
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
|Feature=HSL and HSLa
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
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
|External_links=* [http://dev.opera.com/articles/view/color-in-opera-10-hsl-rgb-and-alpha-transparency/ http://dev.opera.com/articles/view/color-in-opera-10-hsl-rgb-and-alpha-transparency/]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}