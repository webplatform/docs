{{Page_Title|alignment-adjust}}
{{Flags
|High-level issues=Stub
|Content=Incomplete
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>alignment-adjust</code> property allows more precise alignment of elements, such as graphics, that do not have a baseline-table or lack the desired baseline in their baseline-table. With the <code>alignment-adjust</code> property, the position of the baseline identified by the <code>alignment-adjust</code> can be explicitly determined. It also determines precisely the alignment point for each glyph within a textual element. The user agent should use heuristics to determine the position of a non existing baseline for a given element.}}
{{CSS Property
|Initial value=auto
|Applies to=inline-level elements
|Inherited=No
|Media=visual
|Computed value=see text
|Animatable=No
|CSS percentages=refers to the 'line-height' of the element
|Values={{CSS Property Value
|Data Type=baseline
|Description=The alignment point is at the intersection of the start-edge of the element and the dominant-baseline of the element.
}}{{CSS Property Value
|Data Type=before-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the before-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.
}}{{CSS Property Value
|Data Type=text-before-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the 'text-before-edge' baseline of the element.
}}{{CSS Property Value
|Data Type=central
|Description=The alignment point is at the intersection of the start-edge of the element and the 'central' baseline of the element.
}}{{CSS Property Value
|Data Type=middle
|Description=The alignment point is at the intersection of the start-edge of the element and the 'middle' baseline of the element.
}}{{CSS Property Value
|Data Type=after-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the after-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.
}}{{CSS Property Value
|Data Type=text-after-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the 'text-after-edge' baseline of the element.
}}{{CSS Property Value
|Data Type=ideographic
|Description=The alignment point is at the intersection of the start-edge of the element and the 'ideographic' baseline of the element.
}}{{CSS Property Value
|Data Type=alphabetic
|Description=The alignment point is at the intersection of the start-edge of the element and the 'alphabetic' baseline of the element.
}}{{CSS Property Value
|Data Type=hanging
|Description=The alignment point is at the intersection of the start-edge of the element and the 'hanging' baseline of the element.
}}{{CSS Property Value
|Data Type=mathematical
|Description=The alignment point is at the intersection of the start-edge of the element and the 'mathematical' baseline of the element.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The computed value of the property is this percentage multiplied by the computed 'line-height' of the element. The alignment point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the computed value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of '0%' makes the dominant-baseline the alignment point.
}}{{CSS Property Value
|Data Type=<length>
|Description=The alignment-point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the <length> value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of '0cm' makes the dominant-baseline the alignment point.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;p&gt;
	alignment-adjust CSS property:
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 1&quot; class=&quot;image1&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 2&quot; class=&quot;image2&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 3&quot; class=&quot;image3&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 4&quot; class=&quot;image4&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 5&quot; class=&quot;image5&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 6&quot; class=&quot;image6&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 7&quot; class=&quot;image7&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 8&quot; class=&quot;image8&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 9&quot; class=&quot;image9&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 10&quot; class=&quot;image10&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 11&quot; class=&quot;image11&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 12&quot; class=&quot;image12&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 13&quot; class=&quot;image13&quot;&gt;
	&lt;img src=&quot;http://placehold.it/40x40&quot; alt=&quot;Image 14&quot; class=&quot;image14&quot;&gt;
&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/6363838
}}{{Single Example
|Language=CSS
|Code=/**
 * alignment-adjust
 * CSS3 property
 * http://docs.webplatform.org/w/index.php?title=css/properties/alignment-adjust
 */

p {
	border: 1px dotted #ddd;
	color: #222;
	font: 1em/5em 'Open Sans', sans-serif;
	padding: 0.5em;
}

p img {
	vertical-align: middle;
}

p img:first-child {
	margin-left: 1em;
}

.image1 { alignment-adjust: auto; }
.image2 { alignment-adjust: baseline; }
.image3 { alignment-adjust: before-edge; }
.image4 { alignment-adjust: text-before-edge; }
.image5 { alignment-adjust: central; }
.image6 { alignment-adjust: middle; }
.image7 { alignment-adjust: after-edge; }
.image8 { alignment-adjust: text-after-edge; }
.image9 { alignment-adjust: ideographic; }
.image10 { alignment-adjust: alphabetic; }
.image11 { alignment-adjust: hanging; }
.image12 { alignment-adjust: mathematical; }
.image13 { alignment-adjust: 75%; }
.image14 { alignment-adjust: -20px; }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 module: line
|URL=http://www.w3.org/TR/css3-linebox/#alignment-adjust-prop
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout
|External_links=* [http://meyerweb.com/eric/css/tests/css3/show.php?p=alignment-adjust alignment-adjust by Eric Meyer]

}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}