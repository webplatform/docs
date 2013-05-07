{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''align-content''' property aligns a flex container's lines within the flex container when there is extra space in the cross-axis, similar to how [[css/properties/justify-content|justify-content]] aligns individual items within the main-axis.}}
{{CSS Property
|Initial value=stretch
|Applies to=multi-line flex containers
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=alignContent
|Values={{CSS Property Value
|Data Type=flex-start
|Description=Lines are packed toward the start of the flex container. The cross-start edge of the first line in the flex container is placed flush with the cross-start edge of the flex container, and each subsequent line is placed flush with the preceding line.
}}{{CSS Property Value
|Data Type=flex-end
|Description=Lines are packed toward the end of the flex container. The cross-end edge of the last line is placed flush with the cross-end edge of the flex container, and each preceding line is placed flush with the subsequent line.
}}{{CSS Property Value
|Data Type=center
|Description=Lines are packed toward the center of the flex container. The lines in the flex container are placed flush with each other and aligned in the center of the flex container, with equal amounts of empty space between the cross-start content edge of the flex container and the first line in the flex container, and between the cross-end content edge of the flex container and the last line in the flex container. (If the leftover free-space is negative, the lines will overflow equally in both directions.)
}}{{CSS Property Value
|Data Type=space-between
|Description=Lines are evenly distributed in the flex container. If the leftover free-space is negative this value is identical to '''flex-start'''. Otherwise, the cross-start edge of the first line in the flex container is placed flush with the cross-start content edge of the flex container, the cross-end edge of the last line in the flex container is placed flush with the cross-end content edge of the flex container, and the remaining lines in the flex container are distributed so that the empty space between any two adjacent lines is the same.
}}{{CSS Property Value
|Data Type=space-around
|Description=Lines are evenly distributed in the flex container, with half-size spaces on either end. If the leftover free-space is negative this value is identical to '''center'''. Otherwise, the lines in the flex container are distributed such that the empty space between any two adjacent lines is the same, and the empty space before the first and after the last lines in the flex container are half the size of the other empty spaces.
}}{{CSS Property Value
|Data Type=stretch
|Description=Lines stretch to take up the remaining space. If the leftover free-space is negative, this value is identical to '''flex-start'''. Otherwise, the free-space is split equally between all of the lines, increasing their cross size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Spacing lines within a multi-line flex container.
|Code=.container {
  display: -webkit-flex;
  display:    -moz-flex;
  display:     -ms-flex;
  display:      -o-flex;
  display:         flex;
  
  -webkit-flex-flow: row wrap;
     -moz-flex-flow: row wrap;
      -ms-flex-flow: row wrap;
       -o-flex-flow: row wrap;
          flex-flow: row wrap;
          
  -webkit-align-content: space-around; /*  values: flex-start, flex-end, center, space-between, space-around, stretch */ 
     -moz-align-content: space-around;
      -ms-align-content: space-around;
       -o-align-content: space-around;
          align-content: space-around;
  
  width: 400px;
  height: 200px;
  background: #CCC;
}

.container div {
    height: 30px;
    margin: 0px;
}

.container .third-item {
  width: 160px;
  background: #CC3333;
  font-size: 14px;  
}

.container .second-item {
  width: 140px;
  background: #FFFC33;
}

.container .first-item {
  width: 100px;
  background: #3333FF;
}
|LiveURL=http://code.webplatform.org/gist/5536244
}}
}}
{{Notes_Section
|Notes=Note, this property has no effect when the flexbox has only a single line. Only flex containers with multiple lines ever have free space in the cross-axis for lines to be aligned in, because in a flex container with a single line the sole line automatically stretches to fill the space.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#align-content-property
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=http://caniuse.com/#flexbox
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Flexbox
|External_links=Also, check out the following live demo sites:
* [http://demo.agektmr.com/flexbox/ Flexbox Playground]
* [http://the-echoplex.net/flexyboxes Flexy Boxes]
}}
{{Topics|CSS, Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}