{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
|Editorial notes='''As of time of writing, this property is not yet implemented in most browsers.'''
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies how mask images are tiled (repeated) after they have been sized and positioned.|Specifies how mask images are tiled after they have been sized and positioned_ Where 
<repeat-style>=repeat-x
}}
{{CSS Property
|Initial value=no-repeat
|Applies to=All elements. In SVG, it applies to container elements without the <defs> element and all graphics elements.
|Inherited=No
|Media=visual
|Computed value=A list, each item consisting of two keywords, one per dimension
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<repeat-style>
|Description=The repeating behavior of the mask, as in the CSS <code>background-repeat</code> property. Single values for <repeat-style> are:
*'''repeat-x''': Tiling of the mask object occurs in the x direction.
*'''repeat-y''': Tiling of the mask object occurs in the y direction.
*'''repeat''': Tiling of the mask object occurs in both the x and y directions as often as needed to cover the background area.
*'''space''': Tiling of the mask object occurs in both the x and y directions as often as will fit within the background positioning area without being clipped, and then the images are spaced out to fill the area.
*'''round''': Tiling of the mask object occurs in both the x and y directions as often as will fit within the background positioning area. If it does not fit a whole number of times, it is rescaled so that it does. 
*'''no-repeat''': Tiling of the mask object does not occur; that is, it is placed once and not repeated.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* repeat-y */
body {
  background-color: white;
  mask-image: url(dot-mask.png);
  mask-position: center;
  mask-repeat: repeat-y;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=https://dvcs.w3.org/hg/FXTF/raw-file/default/masking/index.html
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}