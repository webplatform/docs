{{Page_Title}}
{{Flags
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
|Description=An example with the justify-content property, demonstrating the different options.
|Code=.container {
  display: -webkit-flex;
  display:    -moz-flex;
  display:     -ms-flex;
  display:      -o-flex;
  display:         flex;
  
  width: 800px;
  height: 100px;
  background: #CCC;
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

.third-item {
  width: 150px;
  background: #CC3333;

}

.second-item {
  width: 275px;
  background: #FFFC33;
}

.first-item {
  width: 200px;
  background: #3333FF;
}

.flex-start {
  -webkit-justify-content: flex-start;
     -moz-justify-content: flex-start;
      -ms-justify-content: flex-start;
       -o-justify-content: flex-start;
          justify-content: flex-start; 
}

.flex-end {
    justify-content: flex-end; 
}

.justifycenter {
    justify-content: center; 
}

.space-around {
    justify-content: space-around; 
}

.space-between {
    justify-content: space-between; 
}
|LiveURL=http://code.webplatform.org/gist/5842739
}}{{Single Example
|Language=HTML
|Code=&lt;p&gt;justify-content: flex-start&lt;/p&gt;
&lt;div class="container flex-start"&gt;
  &lt;div class="first-item"&gt;first-item&lt;/div&gt;
  &lt;div class="second-item"&gt;second-item&lt;/div&gt;
  &lt;div class="third-item"&gt;third-item&lt;/div&gt;
&lt;/div&gt;
&lt;p&gt;justify-content: flex-end&lt;/p&gt;
&lt;div class="container flex-end"&gt;
  &lt;div class="first-item"&gt;first-item&lt;/div&gt;
  &lt;div class="second-item"&gt;second-item&lt;/div&gt;
  &lt;div class="third-item"&gt;third-item&lt;/div&gt;
&lt;/div&gt;
&lt;p&gt;justify-content: center&lt;/p&gt;
&lt;div class="container justifycenter"&gt;
  &lt;div class="first-item"&gt;first-item&lt;/div&gt;
  &lt;div class="second-item"&gt;second-item&lt;/div&gt;
  &lt;div class="third-item"&gt;third-item&lt;/div&gt;
&lt;/div&gt;
&lt;p&gt;justify-content: space-around&lt;/p&gt;
&lt;div class="container space-around"&gt;
  &lt;div class="first-item"&gt;first-item&lt;/div&gt;
  &lt;div class="second-item"&gt;second-item&lt;/div&gt;
  &lt;div class="third-item"&gt;third-item&lt;/div&gt;
&lt;/div&gt;
&lt;p&gt;justify-content: space-between&lt;/p&gt;
&lt;div class="container space-between"&gt;
  &lt;div class="first-item"&gt;first-item&lt;/div&gt;
  &lt;div class="second-item"&gt;second-item&lt;/div&gt;
  &lt;div class="third-item"&gt;third-item&lt;/div&gt;
&lt;/div&gt;
}}
}}
{{Notes_Section
|Notes=This property was named '''flex-pack''' in earlier drafts.
}}
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
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=12
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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