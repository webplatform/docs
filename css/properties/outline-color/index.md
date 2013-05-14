{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The outline-color property sets the color of the [[css/properties/outline|outline]] of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.}}
{{CSS Property
|Initial value=invert
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=The computed value for ‘invert’ is ‘invert’. For <color> values, the computed value is as defined for the ‘color’ property.
|Animatable=Yes
|CSS object model property=outlineColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<color>
|Description=Specify the color to use on all outlines. This can be anywhere from one to four values representing the top, right, bottom, and left outline respectively.
}}{{CSS Property Value
|Data Type=invert
|Description=This is expected to perform a color inversion on the pixels on the screen.
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that the value is inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=An example of using outline color
|Code=&lt;div class=&quot;outline&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt; 
&lt;div class=&quot;outline outline--blue&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;outline outline--green&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt; 
&lt;div class=&quot;outline outline--invert&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5566688
}}{{Single Example
|Language=CSS
|Description=Multiple classes that change the original outline color
|Code=/*
  outline color example
*/

.outline--green {
  /* make the outline red */
  outline-color: #00ff00;
}

.outline--blue {
  /* make the outline blue */
  outline-color: #0000ff;
}

.outline--invert {
	/* outline invert */
	outline-color: invert;
}
|LiveURL=http://code.webplatform.org/gist/5566688
}}
}}
{{Notes_Section
|Usage=The color value can be a numerical value, such as one of the following:

* a basic color keyword, such as "red"
* a hex value, such as #ff0000
* an red-green-blue (RGB) value, such as rgb(255,0,0)
* an RGB-alpha (RGBA) that includes color opacity, such as rgba(255,0,0,1) or rgba(100%,0%,0%,1)
* a hue-saturation-lightness (HSL), such as hsl(0, 100%, 50%)
* HSLa, such as hsl(0, 100%, 50%, 1)

The color value can also be an extended keyword, such as aliceblue or lavenderblush. For a full list of extended keywords, see the [http://www.w3.org/TR/css3-color/#svg-color CSS Color Module Level 3 spec], which is the consolidation of various specifications.
|Notes=* A value of '''invert''' ensures that the outline is visible regardless of the background color.
* The [[css/properties/outline|outline]] property is a shorthand property for setting one or more of the individual outline properties [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] and [[css/properties/outline-color|outline-color]] in a single rule. In most cases the use of this shortcut is preferable and more convenient.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 UI, 7.4. ‘outline-color’ property
|URL=http://dev.w3.org/csswg/css-ui/#outline-color
|Status=Working Draft
}}{{Related Specification
|Name=CSS 2.1, 18.4 Dynamic outlines: the 'outline' property
|URL=http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/outline-color
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}