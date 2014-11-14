{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This background property is a shorthand property for setting the color, position, size, repeat, clip, origin, attachment, and image of the element.

The background- properties provide fundamental styles to an element, such as color, image, and position. CSS3 adds more properties for handling backgrounds, including properties that improve the mobile web experience. Many CSS background properties can be set, at the same time, with this background property.
}}
{{CSS Property
|Initial value=see individual properties: * [[css/properties/background-color|background-color]] * [[css/properties/background-position|background-position]] * [[css/properties/background-size|background-size]] * [[css/properties/background-repeat|background-repeat]] * [[css/properties/background-attachment|background-attachment]] * [[css/properties/background-clip|background-clip]] * [[css/properties/background-origin|background-origin]] * [[css/properties/background-image|background-image]]
|Applies to=all elements
|Inherited=No
|Media=visual
|Computed value=see individual properties
|Animatable=No
|CSS object model property=background
|CSS percentages=see individual properties
|Values={{CSS Property Value
|Data Type=<bg-image>
|Description=Any of the values available to [[css/properties/background-image|'''background-image''']] property. The default value is <tt>none</tt>.
}}{{CSS Property Value
|Data Type=<position> [ / <bg-size> ]?
|Description=Any of the values available to [[css/properties/background-position|'''background-position''']] property. Otherwise, it is set to its initial value.
}}{{CSS Property Value
|Data Type=<repeat-style>
|Description=Any of the values available to [[css/properties/background-repeat|'''background-repeat''']] property. The default value is <tt>repeat</tt>.
}}{{CSS Property Value
|Data Type=<attachment>
|Description=Any of the values available to [[css/properties/background-attachment|'''background-attachment''']] property. The default value is <tt>scroll</tt>.
}}{{CSS Property Value
|Data Type=<box>&#123;1,2&#125;
|Description=If one <box> value is present then it sets both [[css/properties/background-origin|'''background-origin''']] and [[css/properties/background-clip|'''background-clip''']] to that value. If two values are present, then the first sets [[css/properties/background-origin|'''background-origin''']] and the second [[css/properties/background-clip|'''background-clip''']].

For background-clip, valid values are those available to [[css/properties/background-clip|'''background-clip''']] property. The default value is <tt>border-box</tt>.
For background-origin, valid values are those  available to [[css/properties/background-origin|'''background-origin''']] property. The default value is <tt>padding-box</tt>.
}}{{CSS Property Value
|Data Type=<color>
|Description=Any of the values available to [[css/properties/background-color|'''background-color''']] property. The default value is <tt>transparent</tt>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The background property is set to the color #f06 on the p element.
|Code=p {
	background: #f06;
}
|LiveURL=http://code.webplatform.org/gist/6114809
}}{{Single Example
|Language=CSS
|Description=Only one background property is set on the body. Many individual properties have been specified for the p element, including a background image that only shows up on the p element.
|Code=body { 
	background: #90ee90;
	font-family: 'Bitter';

}
p { background: url(http://www.webplatform.org/logo/wplogo_transparent_xlg.png) 
				40% / 20em
				#ffffe0
				round
				fixed
				border-box; 
}
|LiveURL=http://code.webplatform.org/gist/6115439
}}
}}
{{Notes_Section
|Usage=The background property is a shorthand property that can set almost all of the background- properties. The [http://www.w3.org/TR/css3-background/#background specification] has examples of how to use the shorthand property and what that usage translates to.
|Notes=The background of the root element becomes the background of the canvas and extends to cover the entire canvas, but only for that element alone. For an example, see [http://code.webplatform.org/gist/6115439].

Internationalization topics related to the <code>background</code> property:
* [http://localhost/International/techniques/authoring-html#textexpansion Preparing for text expansion]
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3
|URL=http://www.w3.org/TR/css3-background/
|Status=Candidate Recommendation
|Relevant_changes=Introduced background-size, background-clip, background-origin, extended background-position and background-attachment
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS21/colors.html#propdef-background
|Status=Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Background
|Manual_links=* [[tutorials/using_css_multiple_background|Using Multiple Backgrounds]]
* [[tutorials/CSS_background_images|CSS_background_images]]
|External_links=* [http://coding.smashingmagazine.com/2009/09/02/backgrounds-in-css-everything-you-need-to-know/ Backgrounds In CSS: Everything You Need To Know], By Michael Martin
* [http://updates.html5rocks.com/2013/02/CSS-Background-shorthand-coming-to-mobile-WebKit-browsers CSS Background shorthand coming to mobile WebKit browsers], By Stephen Thomas
* [http://mobile.smashingmagazine.com/2013/07/22/simple-responsive-images-with-css-backgrounds/ Simple Responsive Images With CSS Background Images], By Stephen Thomas
* [http://css-tricks.com/just-one-of-those-weird-things-about-css-background-on-body/ Just One of Those Weird Things About CSS: Background on body], By Chris Coyier
* [http://css-tricks.com/almanac/properties/b/background/ background], By Chris Coyier
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}