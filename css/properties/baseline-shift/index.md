{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Obsoleted - spec retired, not implemented.}}
{{CSS Property
|Initial value=baseline
|Applies to=inline-level elements
|Inherited=No
|Media=visual
|Computed value=see text
|Animatable=No
|Values={{CSS Property Value
|Data Type=baseline
|Description=There is no baseline shift; the dominant baseline remains in its original position.
}}{{CSS Property Value
|Data Type=sub
|Description=The dominant baseline is shifted to the default position for subscripts. The offset for this position is determined by the font data for the parent nominal font as adjusted by the dominant baseline-table font-size of the parent element. If there is no applicable font data the User Agent may use heuristic to determine the offset.
}}{{CSS Property Value
|Data Type=super
|Description=The dominant baseline is shifted to the default position for superscripts. The offset for this position is determined by the font data for the parent nominal font as adjusted by the dominant baseline-table font-size of the parent element. If there is no applicable font data the User Agent may use heuristic to determine the offset.
}}{{CSS Property Value
|Data Type=&lt;percentage&gt;
|Description=The computed value of the property is this percentage multiplied by the computed 'line-height' of the parent element. The dominant-baseline is shifted in the shift-direction (positive value) or opposite to the shift-direction (negative value) of the parent area by the computed value. A value of '0%' is equivalent to 'baseline'.
}}{{CSS Property Value
|Data Type=&lt;length&gt;
|Description=The dominant-baseline is shifted in the shift-direction (positive value) or opposite to the shift-direction (negative value) of the parent area by the <length> value. A value of '0cm' is equivalent to 'baseline'.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This property works with HTML inline-level elements.
|Code=&lt;span&gt; I really love Webplatform.docs &lt;/span&gt;
|LiveURL=http://code.webplatform.org/gist/7001747
}}{{Single Example
|Language=CSS
|Description=In this sample, baseline-shift has the value 'baseline' which is the initial value, keeping the baseline in its original position.
|Code=span {
	baseline-shift: baseline;
}
}}{{Single Example
|Language=CSS
|Description=In this sample, the baseline-shift has the value 'sub', putting the text in the subscript position.
|Code=span {
	baseline-shift: sub;
}
}}{{Single Example
|Language=CSS
|Description=In this sample, the baseline-shift has the value 'super', putting the text in the superscript position.
|Code=span {
	baseline-shift: super;
}
}}{{Single Example
|Language=CSS
|Description=This sample show that it's possible to use this property with percentage values.
|Code=/* Percentage values are composed by a number and the '%' symbol */
/* A value of '0%' is equivalent to 'baseline' */
span {
	baseline-shift: 10%;
}
}}{{Single Example
|Language=CSS
|Description=Also, it's possible to use length units as values for the 'baseline-shift' property, as shown the next sample.
|Code=/* Length values are composed by a number and the unit symbol (e. g., 'px', 'em', 'cm', etc) */
span {
	baseline-shift: 2em;
}
}}
}}
{{Notes_Section
|Notes=Although it may seem that 'baseline-shift' and 'alignment-adjust' properties are doing the same thing, there are important differences. For 'alignment-adjust' the percentage values refer to the 'line-height' of the element being aligned. For 'baseline-shift the percentage values refer to the 'line-height' of the parent element. Similarly, it is the 'sub' and 'super' offsets of the parent that are used to align the shifted baseline rather than the 'sub' and 'super' offsets of the element being positioned. To ensure a consistent sub- or superscript position, it makes more sense to use the parent as the reference rather than the subscript element which may have a changed "line-height" due to "font-size" changes in the sub- or superscript element.
Using the "alignment-adjust" property is more suitable for positioning elements, such as graphics, that have no internal textual structure. Using the "baseline-shift" property is intended for sub- and superscripts where the positioned element may itself be textual. The baseline-shift provides a way to define a specific baseline offset other than the named offsets that are defined relative to the dominant-baseline. In addition, having "baseline-shift" makes it easier for a tool to generate the relevant properties; many formatting programs already have a notion of baseline shift.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 module: line
|URL=http://www.w3.org/TR/css3-linebox/#baseline-shift
|Status=Obsoleted (Working Draft)
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}