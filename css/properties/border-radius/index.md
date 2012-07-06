{{CSS Property
|Initial value=0
|Applies to=all elements, except the 'table' element when border-collapse is collapse
|Inherited=Yes
|Media=visual
|Computed value=as specified by individual properties
|Animatable=Yes
|Values={{CSS Property Value
|Description=Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the CSS <length> data types. Negative values are invalid.
}}{{CSS Property Value
|Description=Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axe refer to the width of the box, percentages for the vertical axe refer to the height of the box. Negative values are invalid.
}}
|Syntax=The syntax of the first radius allows one to four values:
* border-radius: radius
* border-radius: top-left-and-bottom-right top-right-and-bottom-left
* border-radius: top-left top-right-and-bottom-left bottom-right
* border-radius: top-left top-right bottom-right bottom-left 

The syntax of the second radius also allows one to four values
* border-radius: (first radius values) / radius
* border-radius: (first radius values) / top-left-and-bottom-right top-right-and-bottom-left
* border-radius: (first radius values) / top-left top-right-and-bottom-left bottom-right
* border-radius: (first radius values) / top-left top-right bottom-right bottom-left

border-radius: inherit
|Value_Name=percentage
}}
== Example ==

<syntaxhighlight lang="css" line start="0" highlight="2">
solid 10px;
border-radius: 40px 10px;
</syntaxhighlight>


{{Major_Style_Issue|main_message=This article does not include a complete compatibility table.}}