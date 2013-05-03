{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''flex-shrink''' CSS property specifies how much a flex item will be reduced with respect to the other items in the flex container to fit within a reduced container.}}
{{CSS Property
|Initial value=1
|Applies to=flex items
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|Values={{CSS Property Value
|Data Type=number
|Description=The flex shrink factor, which describes the proportion by which the flex item will shrink relative to the other flex items in the container. Negative numbers are invalid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=See [[css/properties/flex#Examples|flex examples]] for the use of this property in an example.
|Code=flex-shrink: 3;
}}
}}
{{Notes_Section
|Usage=The best practice is to use (instead of this property) the [[css/properties/flex|flex]] shorthand property, as it correctly resets any unspecified flex components to accomodate common uses.
|Notes=This property is animatable only for values of 1 or greater.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Model
|URL=http://dev.w3.org/csswg/css-flexbox/#flex-shrink
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=css/properties/flex
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Flexbox
}}
{{Topics|Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}