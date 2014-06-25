{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies the maximum amount of trailing whitespace (before justification) that may be left in a line before hyphenation is triggered to pull part of a word from the next line back up into the current one.}}
{{CSS Property
|Initial value=0
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=hyphenateLimitZone
|CSS percentages=refer to width of the line box
|Values={{CSS Property Value
|Data Type=percentage
|Description=Specifies the width of the hyphenation zone, relative to the total line length. Negative values are not allowed.
}}{{CSS Property Value
|Data Type=length
|Description=Indicates the width of the hyphenation zone. Lengths set in font-relative units (em, ex, ch) tend to be more useful here. Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Only hyphenate if the line would otherwise be <= 90% its maximum possible width */
hyphenate-limit-zone: 10%;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Level 4
|URL=http://dev.w3.org/csswg/css-text-4/#hyphenate-limit-zone
|Status=W3C Editor’s Draft
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
|Topic_clusters=Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}