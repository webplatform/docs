{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''flex-basis''' CSS property describes the initial main size of the flex item before any free space is distributed according to the flex factors described in the [[css/properties/flex|flex]] property ([[css/properties/flex-grow|flex-grow]] and [[css/properties/flex-shrink|flex-shrink]]).}}
{{CSS Property
|Initial value=auto
|Applies to=flex items
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=flexBasis
|CSS percentages=relative to the main size of the flex container
|Values={{CSS Property Value
|Data Type=auto
|Description=The flex item's initial main size is determined by either the [[css/properties/width|width]] or [[css/properties/height|height]] property, whichever is in the main dimension, as determined by the [[css/properties/flex-flow|flex-direction]] property. Note that the value of the [[css/properties/width|width]] or [[css/properties/height|height]] property itself may be '''auto''', in which case the size is determined by the flex item's contents.
}}{{CSS Property Value
|Data Type=width
|Description=In a horizontal writing mode; percentage values of '''flex-basis''' are resolved against the flex item's flex container, and if that containing block's size is indefinite, the result is undefined.
}}{{CSS Property Value
|Data Type=height
|Description=In a vertical writing mode; percentage values of '''flex-basis''' are resolved against the flex item's flex container, and if that containing block's size is indefinite, the result is undefined.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=See [[css/properties/flex#Examples|flex examples]] for the use of this property in an example.
|Code=flex-basis: 60%;
}}
}}
{{Notes_Section
|Usage=The best practice is to use (instead of this property) the [[css/properties/flex|flex]] shorthand property, as it correctly resets any unspecified flex components to accomodate common uses.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Model
|URL=http://dev.w3.org/csswg/css-flexbox/#flex-basis
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