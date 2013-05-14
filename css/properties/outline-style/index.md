{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The outline-style property sets the style of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=Specified value
|Animatable=No
|CSS object model property=outlineStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Outline is not drawn, color and width are ignored.
}}{{CSS Property Value
|Data Type=dotted
|Description=A series of round or square dots.
}}{{CSS Property Value
|Data Type=dashed
|Description=A series of square-ended dashes.
}}{{CSS Property Value
|Data Type=solid
|Description=A single line segment.
}}{{CSS Property Value
|Data Type=double
|Description=Outline is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/outline-width|outline-width]] value. The border width must be at least 3 pixels wide to draw a double outline.
}}{{CSS Property Value
|Data Type=groove
|Description=Looks as if it were carved in the canvas. (This is typically achieved by creating a “shadow” from two colors that are slightly lighter and darker than the [[css/properties/outline-color|outline-color]].)
}}{{CSS Property Value
|Data Type=ridge
|Description=Looks as if it were coming out of the canvas.
}}{{CSS Property Value
|Data Type=inset
|Description=Looks as if the content on the inside of the outline is sunken into the canvas.
}}{{CSS Property Value
|Data Type=outset
|Description=Looks as if the content on the inside of the outline is coming out of the canvas.
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that the value is inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple showing multiple <span>s.
|Code=<div class="all">
<p>
      <span class="one">One</span>
    </p>
    <p>
      <span class="two">Two</span>
    </p>
    <p>
      <span class="three">Three</span>
    </p>
    <p>
      <span class="four">Four</span>
    </p>
    <p>
      <span class="five">Five</span>
    </p>
    <p>
      <span class="six">Six</span>
    </p>
    <p>
      <span class="seven">Seven</span>
    </p>
    <p>
      <span class="eight">Eight</span>
    </p>
    <p>
      <span class="nine">Nine</span>
    </p>
</div>
|LiveURL=http://code.webplatform.org/gist/5579124
}}{{Single Example
|Language=CSS
|Description=Outline styles in CSS.
|Code=.all {
  background-color: lightgrey;
}

.all p {
  padding: 20px;
}
  
.all span {
  padding: 10px;
  margin: 10px 10px 10px 10px;
  font-size: 36px;
  font-family: Bitter;
  outline-width: 5px;
}

.all .one {
  outline-style: none;
}

.all .two {
  outline-style: outset;
}

.all .three {
  outline-style: dotted;
}

.all .four {
  outline-style: dashed;
}

.all .five {
  outline-style: solid;
}

.all .six {
  outline-style: double;
}

.all .seven {
  outline-style: groove;
}

.all .eight {
  outline-style: ridge;
}

.all .nine {
  outline-style: inset;
}
|LiveURL=http://code.webplatform.org/gist/5579124
}}
}}
{{Notes_Section
|Notes=* This property accepts the same values as [[css/properties/border-style|border-style]], ''' ''except'' ''' that ‘hidden’ is not a legal outline style.
* The [[css/properties/outline|outline]] property is a shorthand property for setting one or more of the individual outline properties [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] and [[css/properties/outline-color|outline-color]] in a single rule. In most cases the use of this shortcut is preferable and more convenient.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic User Interface Module Level 3 (CSS3 UI)
|URL=http://dev.w3.org/csswg/css-ui/#outline-style0
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.5
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}