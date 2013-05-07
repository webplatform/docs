{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''justify-content''' property aligns flex items along the main axis of the current line of the flex container, similarly to how [[css/properties/align-items|align-items]] aligns items in the cross axis.}}
{{CSS Property
|Initial value=flex-start
|Applies to=flex containers
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|Values={{CSS Property Value
|Data Type=flex-start
|Description=Flex items are packed toward the start of the line. The main-start margin edge of the first flex item on the line is placed flush with the main-start edge of the line, and each subsequent flex item is placed flush with the preceding item.
}}{{CSS Property Value
|Data Type=flex-end
|Description=Flex items are packed toward the end of the line. The main-end margin edge of the last flex item is placed flush with the main-end edge of the line, and each preceding flex item is placed flush with the subsequent item.
}}{{CSS Property Value
|Data Type=center
|Description=Flex items are packed toward the center of the line. The flex items on the line are placed flush with each other and aligned in the center of the line, with equal amounts of empty space between the main-start edge of the line and the first item on the line and between the main-end edge of the line and the last item on the line. (If the leftover free-space is negative, the flex items will overflow equally in both directions.)
}}{{CSS Property Value
|Data Type=space-between
|Description=Flex items are evenly distributed in the line. If the leftover free-space is negative or there is only a single flex item on the line, this value is identical to ‘flex-start’. Otherwise, the main-start margin edge of the first flex item on the line is placed flush with the main-start edge of the line, the main-end margin edge of the last flex item on the line is placed flush with the main-end edge of the line, and the remaining flex items on the line are distributed so that the spacing between any two adjacent items is the same.
}}{{CSS Property Value
|Data Type=space-around
|Description=Flex items are evenly distributed in the line, with half-size spaces on either end. If the leftover free-space is negative or there is only a single flex item on the line, this value is identical to ‘center’. Otherwise, the flex items on the line are distributed such that the spacing between any two adjacent flex items on the line is the same, and the spacing between the first/last flex items and the flex container edges is half the size of the spacing between flex items.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=An example with the justify-content property. Open the live example, and substitute the value yourself to see the behavior.
|Code=.container {
  display: -webkit-flex;
  display:    -moz-flex;
  display:     -ms-flex;
  display:      -o-flex;
  display:         flex;
  
  width: 800px;
  height: 100px;
  background: #CCC;
  
  -webkit-justify-content: space-around;
     -moz-justify-content: space-around;
      -ms-justify-content: space-around;
       -o-justify-content: space-around;
          justify-content: space-around; 
}

.container div {
  -webkit-flex: 0;
     -moz-flex: 0;
      -ms-flex: 0;
       -o-flex: 0;
          flex: 0;
 
    height: 100px;
    margin: 0px;
    font-family: Bitter;
    font-size: 24px;
}

.container .third-item {
  width: 150px;
  background: #CC3333;

}

.container .second-item {
  width: 275px;
  background: #FFFC33;
}

.container .first-item {
  width: 200px;
  background: #3333FF;
}
|LiveURL=http://code.webplatform.org/gist/5528710
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://dev.w3.org/csswg/css-flexbox/#justify-content-property
|Status=Candidate Recommendation
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