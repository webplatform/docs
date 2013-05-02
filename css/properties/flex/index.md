{{Page_Title|flex}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''flex''' CSS property specifies the ability of a flex item to alter its dimensions to fill the available space. '''flex''' is a shorthand property comprised of the [[css/properties/flex-grow|flex-grow]], [[css/properties/flex-shrink|flex-shrink]], and [[css/properties/flex-basis|flex-basis]] properties. A flex item can be stretched to use available space proportional to its flex grow factor, or reduced proportional to its flex shrink factor to prevent overflow.}}
{{CSS Property
|Initial value=0 1 auto
|Applies to=flex items
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Equivalent to '''0 0 auto'''
No 
}}{{CSS Property Value
|Data Type=auto
|Description=Equivalent to '''1 1 auto'''
}}{{CSS Property Value
|Data Type=initial
|Description=Equivalent '''0 1 auto''''
}}{{CSS Property Value}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=* The initial values of [[css/properties/flex-grow|flex-grow]] and  [[css/properties/flex-basis|flex-basis]] are different from their defaults when omitted in the '''flex''' shorthand.
* When specifying only the flex-basis, a unitless zero not preceded by two flex factor values, for example '''0&nbsp;&nbsp;''' will be interpreted as a flex factor (probably flex-grow). If you wish to specify only the flex-basis, you must a unit, for example, a percentage.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://dev.w3.org/csswg/css-flexbox/#flex
|Status=Candidate Recommendation
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
|Topic_clusters=Flexbox
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}