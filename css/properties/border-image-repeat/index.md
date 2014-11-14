{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>border-image-repeat</code> CSS property defines how the middle part of a border image is handled to match the size of the border. It has a one-value syntax which describes the behavior for all sides, and a two-value syntax that sets a different value for the horizontal and vertical behavior.}}
{{CSS Property
|Initial value=stretch
|Applies to=all elements, except table elements when border-collapse is collapse
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=borderImageRepeat
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=stretch
|Description=Is a keyword indicating that the image will be stretched to fit the gap between the borders.
}}{{CSS Property Value
|Data Type=repeat
|Description=Is a keyword indicating that the image will be repeated until it fit the gap between the borders
}}{{CSS Property Value
|Data Type=round
|Description=Is a keyword indicating that the image will be repeated until it fit the gap between the borders. If it doesn't fit after having being repeated an integer number of times, it is rescaled to do so.
}}{{CSS Property Value
|Data Type=space
|Description=Is a keyword indicating that the image will be repeated until it fit the gap between the borders. If it doesn't fit after having being repeated a whole number of times, the white space is distributed around the tiles.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;div&gt;s, identical in style except that they have different border-image-repeat properties applied to them.
|Code=&lt;div class="pattern repeat"&gt;Repeat&lt;/div&gt;
&lt;div class="pattern stretch"&gt;Stretch&lt;/div&gt;
&lt;div class="pattern round"&gt;Round&lt;/div&gt;
&lt;div class="pattern space"&gt;Space&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5620804
}}{{Single Example
|Language=CSS
|Description=
|Code=/* This general class will apply the pattern to the containers */
.pattern {
	border-image-source: url(http://docs.webplatform.org/w/images/d/d8/border-image.png);
	border-image-slice: 30;
	border-image-width: 6;
	border-image-outset: 3;	
}

/* Repeat Pattern */
.pattern.repeat{
	border-image-repeat: repeat;
}

/* Stretch Pattern */
.pattern.stretch{
	border-image-repeat: stretch;
}

/* Round Pattern
   Currently available on Gecko browsers (eg: Firefox) */
.pattern.round{
	border-image-repeat: round;
}

/* Space Repeat Setting
   Currently unavailable on all browsers */
.pattern.space{
	border-image-repeat: space;
}
|LiveURL=http://code.webplatform.org/gist/5620804
}}{{Single Example
|Language=
|Description=
|Code=[[File:border-image.png|border-image demo image]]

<code>border-image-repeat: stretch;</code>
[[File:bi-stretch.png|border-image stretch demo]]

<code>border-image-repeat: repeat;</code>
[[File:bi-repeat.png|border-image repeat demo]]

<code>border-image-repeat: round;</code>
[[File:bi-round.png|border-image round demo]]
/* Round is supported by Gecko-based browsers only, like Firefox */

<code>border-image-repeat: space;</code>
[[File:bi-space.png|border-image space demo]]

/* Space is not supported by any browser */
|LiveURL=
}}
}}
{{Notes_Section
|Usage=If one velue is specified, it is used for all four sides. If two values are specified, the first is used for the horizontal sides, and the second is used for vertical ones.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Backgrounds and Borders Module
|URL=http://www.w3.org/TR/css3-background/#the-border-image-repeat
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_links=* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-repeat
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