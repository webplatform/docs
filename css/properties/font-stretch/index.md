{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Allows you to expand or condense the widths for a normal, condensed, or expanded font face.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=ultra-condensed
|Description=This is the most condensed setting.
}}{{CSS Property Value
|Data Type=extra-condensed
|Description=This is the second most condensed setting.
}}{{CSS Property Value
|Data Type=condensed
|Description=Some font faces incorporate a condensed option, this is the equivalent of that setting.
}}{{CSS Property Value
|Data Type=semi-condensed
|Description=This is the least condensed setting.
}}{{CSS Property Value
|Data Type=normal
|Description=This is the default setting.
}}{{CSS Property Value
|Data Type=semi-expanded
|Description=This is the least expanded setting.
}}{{CSS Property Value
|Data Type=expanded
|Description=Some font faces incorporate an expanded option, this is the equivalent of that setting.
}}{{CSS Property Value
|Data Type=extra-expanded
|Description=This is the second most expanded setting.
}}{{CSS Property Value
|Data Type=ultra-expanded
|Description=This is the most expanded setting.
}}{{CSS Property Value
|Data Type=wider (Internet Explorer only)
|Description=This expands the font face in Internet Explorer only.
}}{{CSS Property Value
|Data Type=narrower (Internet Explorer only)
|Description=This condenses the font face in Internet Explorer only.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.ultra-condensed{
	-webkit-font-stretch:ultra-condensed;
	-ms-font-stretch:ultra-condensed;
	-moz-font-stretch:ultra-condensed;
	-o-font-stretch:ultra-condensed;
	font-stretch:ultra-condensed;
	}
.condensed{
	-webkit-font-stretch:condensed;
	-ms-font-stretch:condensed;
	-moz-font-stretch:condensed;
	-o-font-stretch:condensed;
	font-stretch:condensed;
	}
.normal{
	-webkit-font-stretch:normal;
	-ms-font-stretch:normal;
	-moz-font-stretch:normal;
	-o-font-stretch:normal;
	font-stretch:normal;
	}
.expanded{
	-webkit-font-stretch:expanded;
	-ms-font-stretch:expanded;
	-moz-font-stretch:expanded;
	-o-font-stretch:expanded;
	font-stretch:expanded;
	}
.ultra-expanded{
	-webkit-font-stretch:ultra-expanded;
	-ms-font-stretch:ultra-expanded;
	-moz-font-stretch:ultra-expanded;
	-o-font-stretch:ultra-expanded;
	font-stretch:ultra-expanded;
	}
|LiveURL=http://code.webplatform.org/gist/5842671
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''font-stretch: '''normal '''{{!}}''' wider '''{{!}}''' narrower '''{{!}}''' ultra-condensed '''{{!}}''' extra-condensed '''{{!}}''' condensed '''{{!}}''' semi-condensed '''{{!}}''' semi-expanded '''{{!}}''' expanded '''{{!}}''' extra-expanded '''{{!}}''' ultra-expanded '''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.10
}}
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
{{See_Also_Section
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>style</code>
*<code>[[css/properties/font-size-adjust|font-size-adjust]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}