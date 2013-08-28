{{Page_Title|box-decoration-break}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Breaks a box into fragments creating new borders, padding and repeating backgrounds or lets it stay as a continuous box on a page break, column break, or, for inline elements, at a line break.}}
{{CSS Property
|Initial value=slice
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=clone
|Description=Each box fragment is independently wrapped with the border and padding. The ‘border-radius’ and ‘border-image’ and ‘box-shadow’, if any, are applied to each fragment independently. The background is drawn independently in each fragment of the element. A no-repeat background image will thus be rendered once in each fragment of the element.
}}{{CSS Property Value
|Data Type=slice
|Description=No border and no padding are inserted at a break. No box-shadow is drawn at a broken edge; ‘border-radius’ does not apply to its corners; and the ‘border-image’ is rendered for the whole box as if it were unbroken. The effect is as though the element were rendered with no breaks present, and then sliced by the breaks afterward.

Backgrounds are drawn as if, after the element has been laid out (including any justification, bidi reordering, page breaks, etc.), all the element's box fragments were taken and put one after the other in visual order. The background is applied to the bounding box of this composite box and then the fragments are put back, with each with its share of the background.

For boxes broken across lines, first fragments on the same line are connected in visual order. Then fragments on subsequent lines are ordered according to the element's inline progression direction and aligned on the baseline. For example in a left-to-right containing block (‘direction’ is ‘ltr’), the first fragment is the leftmost fragment on the first line and fragments from subsequent lines are put to the right of it. In a right-to-left containing block, the first fragment is the rightmost on the first line and subsequent fragments are put to the left of it.

For boxes broken across columns, the columns are treated as one continuous element, as if the column boxes were glued together in the block progression direction of the multi-column element. For boxes broken across pages, the page content areas are glued together in the block progression direction of the root element. In these cases, if the box fragments have different widths (heights, if the root element / multi-column element is in a vertical writing mode), then each piece draws its background assuming that the whole element has the same width (height) as this piece. This ensures that right-aligned images stay aligned to the right edge, left-aligned images stay aligned to the left edge, and centered images stay centered.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#box-decoration-break
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://dev.w3.org/csswg/css-backgrounds/#box-decoration-break
|Status=Editor's Draft
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
|Topic_clusters=CSS Layout, Background, Border
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}