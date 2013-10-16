{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Inherited=No
|Animatable=No
|Values=
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
|Description=In this sample, the baseline-shift has the value 'suber', putting the text in the superscript position.
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
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
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