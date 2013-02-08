{{Page_Title}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>border-image-width</code> CSS property defines the offset to use for dividing the border image in nine parts, the top-left corner, central top edge, top-right-corner, central right edge, bottom-right corner, central bottom edge, bottom-left corner, and central right edge. They represent inward distance from the top, right, bottom, and left edges.}}
{{CSS Property
|Initial value=none
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=all length made absolute, or as specified
|Animatable=No
|CSS percentages=Relative to the width, for horizontal effects, or the height, for vertical effects, of the border image area.
|Values={{CSS Property Value
|Data Type=<length>
|Description=Represents the length of the image slice. It can be an absolute or relative length. This length must not be negative.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=Represents the percentage of the image slice relative to the height, or width, of the border image area. The percentage must not be negative.
}}{{CSS Property Value
|Data Type=<number>
|Description=Represents a multiple of the computed value of the element's <code>border-width</code> property to be used as the image slice size. The number must not be negative.
}}{{CSS Property Value
|Data Type=auto
|Description=Indicates that the width, or height, of the image size must be the intrinsic size of that dimension.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=border-image-width: 3;          /* One-value syntax */
border-image-width: 2em 3em;          /* Two-value syntax */
border-image-width: 5% 15% 10%;          /* Three-value syntax */
border-image-width: 5% 2em 10% auto;          /* Four-value syntax */
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
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-width
|MSDN_link=
|HTML5Rocks_link=
}}