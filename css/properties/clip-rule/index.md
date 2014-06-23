{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Clipping crops an graphic, so that only a portion of the graphic is rendered, or filled. This clip-rule property, when used with the [[css/properties/clipPath|clipPath]] property, defines which clip rule, or algorithm, to use when filling the different parts of a graphics.}}
{{CSS Property
|Initial value=nonzero
|Applies to=Graphics elements that are contained within a <clipPath> element.
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=nonzero
|Description=This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the places where a shape segment crosses the ray in a specific direction. When a segment crosses the ray from left to right, the count is incremented; when a segment crosses the ray from right to left, the count is decremented. If the count is zero, the point is outside; if non-zero, it is inside.

See [http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty SVG fill-rule property] for details.
}}{{CSS Property Value
|Data Type=evenodd
|Description=This value defines whether a point is inside or outside the path by drawing a ray from that point to infinity in any direction and counting the number of  shape segments that the ray crosses. If the count is odd, the point is inside; if even, the point is outside.

See [http://www.w3.org/TR/2011/REC-SVG11-20110816/painting.html#FillRuleProperty SVG fill-rule property] for details.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=This example uses the SVG <code>clip-rule</code> property to show the difference in values for overlapping circles. With <code>nonzero</code>, the default, the overlapping area is filled in. With <code>evenodd</code> the overlapping area is removed.
|Code=&lt;svg xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink"
     width="100%" height="100%" viewBox="0 0 140 110"&gt;

  &lt;title&gt;'clip-rule' example&lt;/title&gt;
  
  &lt;style&gt;
    .nonzero {
      clip-rule: nonzero;
    }

    .evenodd {
      clip-rule: evenodd;
    }
  &lt;/style&gt;
  
  &lt;defs&gt;
    &lt;path id="circles"
          d="M25,10 A20,20 0,1 0 25,50 A20,20 1,1 0 25,10 M45,10 A20,20 0,1 0 45,50 A20,20 1,1 0 45,10" /&gt;

    &lt;clipPath id="clip-nonzero"&gt;
      &lt;use class="nonzero"
           xlink:href="#circles" /&gt;
    &lt;/clipPath&gt;
    
    &lt;clipPath id="clip-evenodd"&gt;
      &lt;use class="evenodd"
           xlink:href="#circles" y="50"/&gt;
    &lt;/clipPath&gt;    
  &lt;/defs&gt;  
  
  &lt;!-- non-zero clip-rule --&gt;
  &lt;rect clip-path="url(#clip-nonzero)"
        x="0" y="5" width="70" height="50" 
        fill="cornflowerblue"/&gt;

  &lt;!-- equivalent non-zero fill-rule --&gt;
  &lt;use fill-rule="nonzero" 
       xlink:href="#circles" x="70" y="0" 
       stroke="cornflowerblue" /&gt;
  
  
  &lt;!-- even-odd clip-rule --&gt;
  &lt;rect clip-path="url(#clip-evenodd)"
        x="0" y="55" width="70" height="50" 
        fill="goldenrod"/&gt;

  &lt;!-- equivalent even-odd fill-rule --&gt;
  &lt;use fill-rule="evenodd" 
       xlink:href="#circles" x="70" y="50" 
       stroke="goldenrod" /&gt;
&lt;/svg&gt;
|LiveURL=http://code.webplatform.org/gist/7037715
}}
}}
{{Notes_Section
|Usage=The clip-rule property only applies to graphics elements that are contained within a [[css/properties/clipPath|clipPath]] element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking
|URL=http://dev.w3.org/fxtf/masking/
|Status=Editor's Draft
}}{{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/SVG/
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
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