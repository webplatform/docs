{{Page_Title|border-image-outset}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>border-image-outset</code> property describes, by which amount the border image area extends beyond the border box.}}
{{CSS Property
|Initial value=0
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=all length made absolute, otherwise as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=slice
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box in all four directions.
}}{{CSS Property Value
|Data Type=horizontal
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box in both horizontal directions, left and right.
}}{{CSS Property Value
|Data Type=vertical
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box in both vertical directions, top and bottom.
}}{{CSS Property Value
|Data Type=top
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box past its top edge.
}}{{CSS Property Value
|Data Type=bottom
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box past its bottom edge.
}}{{CSS Property Value
|Data Type=right
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box past its right edge.
}}{{CSS Property Value
|Data Type=left
|Description=Is a [[css/data_types/length|length]] or a percentage of the amount by which the border image area extends beyond the border box past its left edge.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=[[File:bi-outset.png|border-outset visualized]]

<code>border-image-outset: 15px;</code>
}}
}}
{{Notes_Section
|Usage=border-image-outset: sides                  /* One-value syntax   */  E.g. border-image-slice: 30%; 
border-image-outset: vertical horizontal    /* Two-value syntax   */  E.g. border-image-slice: 10% 30%; 
border-image-outset: top vertical bottom    /* Three-value syntax */  E.g. border-image-slice: 30px 30% 45px; 
border-image-outset: top right bottom left  /* Four-value syntax  */  E.g. border-image-slice: 7px 12px 14px 5px;

border-image-outset: inherit
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
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-outset
|MSDN_link=
|HTML5Rocks_link=
}}