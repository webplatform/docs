{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies the minimum number of characters in a hyphenated word}}
{{CSS Property
|Initial value=auto
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=hyphenateLimitChars
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Corresponds to a value of <code>5 2 2</code>, indicating a 5-character word limit, 2 characters required before a hyphenation break, and 2 characters required following a hyphenation break.
}}{{CSS Property Value
|Data Type=[[css/data_types/integer|integer]]
|Description=One to three integer values, corresponding to the word limit, the minimum number of characters required before a hyphenation break, and the minimum number of characters required following a hyphenation break, respectively.

If the third value is missing it is equal to the second.

If the second and third values are missing they are given a value of '''auto'''.

Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Only hyphenate words with >= 6 characters,
   leave at least 3 characters before the hyphen and at least 2 after it */
hyphenate-limit-chars: 6 3 2;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Level 4
|URL=http://dev.w3.org/csswg/css-text-4/#hyphenate-limit-chars
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
|Manual_sections====Related pages ===
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