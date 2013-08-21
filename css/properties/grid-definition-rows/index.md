{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property can specify the length, a percentage of the grid container’s size, a measurement of the contents occupying the row, or a fraction of the free space in the grid. You can also specify a range using minmax(), which combines any of these measurements to define a min and max size for the row.

As well as referring to grid lines by their numerical index, you can also name lines. Names can make the grid-placement properties easier to understand and maintain. Lines can have multiple names, such as 'first' and 'header'.
}}
{{CSS Property
|Initial value=none
|Applies to=grid container
|Inherited=No
|Media=visual
|Computed value=As specified, except for ‘auto’ (see prose)
|Animatable=No
|CSS object model property=gridDefinitionRows
|CSS percentages=n/a
|Values={{CSS Property Value
|Data Type=none
|Description=No initial grid; any rows are implicitly generated with their size determined by the ‘grid-auto-rows’ property.
}}{{CSS Property Value
|Data Type=<track-list>
|Description=The track-list syntax is:

&lt;track-list&gt;    = &#91; &lt;string&gt;* &#91; &lt;track-size&gt; &#124; &lt;repeat-function&gt; &#93; &#93;+ &lt;string&gt;*

&lt;track-size&gt;    = minmax( &lt;track-breadth&gt; , &lt;track-breadth&gt; ) &#124; auto &#124; &lt;track-breadth&gt;

&lt;track-breadth&gt; = &lt;length&gt; &#124; &lt;percentage&gt; &#124; &lt;flex&gt; &#124; min-content &#124; max-content

Where the values are described as:

* &lt;length&gt;
* &lt;percentage&gt;: Percentage values are relative to the extent (logical height) of the grid container in grid row tracks. If the extent of the grid container is an indefinite size, <percentage> values relative to that size are treated as ‘auto’.
* &lt;flex&gt;: A non-negative dimension with the unit "fr". Each <flex> value takes a share of the remaining space in proportion to its value. See Flexible Lengths for more details.
* max-content: Largest max size contribution of the grid items occupying the grid track.
* min-content: Largest min size contribution of the grid items occupying the grid track.
* minmax(min, max): Defines a size range greater than or equal to min and less than or equal to max. If max < min, then max is ignored and ‘minmax(min,max)’ is treated as min.
* auto: Computes to ‘minmax(min-content, max-content)’.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=We define four values corresponding to each row of our grid. First row will be exactly 100 pixels, second row will use flex units and will take one 'fr' of the remaining space but because of the third row which takes up two 'fr'. That means the remaining space will divide on three, and second row will take 1/3 of this, and third row will take 2/3.
|Code=#myGrid {
  display: grid;
  grid-definitions-rows: 100px 1fr 2fr;
}
}}{{Single Example
|Language=CSS
|Description=We define three rows where the first one will adapt to its content, the second will take 250 pixels of the screen and third one will take 50% of its container.
|Code=#myGrid {
  display: grid;
  grid-definitions-rows: auto 250px 50%
}
}}{{Single Example
|Language=CSS
|Description=We can also make use of the min/max values. We define two rows where first one take one 'fr', and the second can use either the minimum content of its size, or the maximum value of 1fr. Notice that we gave names on right lines of each rows. That way we can refer to those lines when we define how space will take their contents.
|Code=#myGrid {
  display: grid;
  grid-definition-rows: 1fr "aside" minmax(min-content, 1fr) "main";
}
}}{{Single Example
|Language=CSS
|Description=At last, `repeat` function can be used to create a repeating sequence.
|Code=#myGrid {
  display: grid;
  grid-definition-rows: repeat(3, 100px 1fr); // which equals to
  grid-definition-rows: 100px, 1fr, 100px, 1fr, 100px, 1fr;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Grid Layout, Track Sizing: the ‘grid-definition-rows’ and ‘grid-definition-columns’ properties
|URL=http://dev.w3.org/csswg/css-grid/#track-sizing
|Status=W3C Editor's Draft
|Relevant_changes=Significant changes, including property name & values
}}{{Related Specification
|Name=CSS Grid Layout, Track Sizing: the ‘grid-definition-rows’ and ‘grid-definition-columns’ properties
|URL=http://www.w3.org/TR/css3-grid-layout/#track-sizing
|Status=W3C Working Draft
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
|Topic_clusters=CSS Layout, Grid Layout
|External_links=<ul>
<li>http://css-tricks.com/almanac/properties/g/grid/</li>
</ul>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}