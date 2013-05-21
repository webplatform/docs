{{Page_Title|border-image-outset}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>border-image-outset</code> property describes, by which amount the border image area extends beyond the border box.}}
{{CSS Property
|Initial value=0
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=all length made absolute, otherwise as specified
|Animatable=No
|CSS object model property=borderImageOutset
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<length>
|Description=Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length). This length must not be negative.
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
}}{{Single Example
|Code=<syntaxHighlight>
border-image-outset: sides                  /* One-value syntax   */  E.g. border-image-slice: 30%; 
border-image-outset: vertical horizontal    /* Two-value syntax   */  E.g. border-image-slice: 10% 30%; 
border-image-outset: top vertical bottom    /* Three-value syntax */  E.g. border-image-slice: 30px 30% 45px; 
border-image-outset: top right bottom left  /* Four-value syntax  */  E.g. border-image-slice: 7px 12px 14px 5px;
</syntaxHighlight>
}}
}}
{{Notes_Section
|Usage=* Up to four different values can be specified, in the following order: top, right, bottom, left.
* If one value is specified, it is used for all four sides. If two values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three values are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-image-outset
|Status=W3C Candidate Recommendation
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
|Topic_clusters=Border
|Manual_links=* [[tutorials/css_border_image|Decorating fancy borders with CSS border-image]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-outset
|MSDN_link=
|HTML5Rocks_link=
}}