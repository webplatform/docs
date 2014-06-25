{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Indicates the maximum number of successive hyphenated lines in an element. The ‘no-limit’ value means that there is no limit.}}
{{CSS Property
|Initial value=no-limit
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=hyphenateLimitLines
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=no-limit
|Description=Indicates that hyphenation is not limited based on the number of consecutive hyphenated lines. In the flow above the consecutive hyphenated lines limit would be an infinitely large positive number.
}}{{CSS Property Value
|Data Type=[[css/data_types/integer|integer]]
|Description=Indicates the maximum number of successive hyphenated lines.

For instance, if <code>2</code>, then no more than 2 successive lines may end with a hyphenated word. If <code>0</code> then no lines may end with a hyphenated word. (Hyphenation is effectively disabled.)

Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Do not allow more than 2 successive hyphenated lines */
hyphenate-limit-lines: 2;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Level 4
|URL=http://dev.w3.org/csswg/css-text-4/#hyphenate-line-limits
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}