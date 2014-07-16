{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The outline-width property sets the width of the [[css/properties/outline|outline]] of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=absolute length; ‘0’ if the outline style is ‘none’.
|Animatable=Yes
|CSS object model property=outlineWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=medium
|Description=Default.  
}}{{CSS Property Value
|Data Type=thin
|Description=Less than the default width.
}}{{CSS Property Value
|Data Type=thick
|Description=Greater than the default width.
}}{{CSS Property Value
|Data Type=<width>
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that the value is inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;span&gt;s.
|Code=&lt;div class="all"&gt;
    &lt;p&gt;
      &lt;span class="medium"&gt;Medium&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="thin"&gt;Thin&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="thick"&gt;Thick&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="width"&gt;10px&lt;/span&gt;
    &lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5579241
}}{{Single Example
|Language=CSS
|Description=CSS outline width values.
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
  outline-style: solid;
}

.all .medium {
  outline-width: medium;
}

.all .thin {
  outline-width: thin;
}

.all .thick {
  outline-width: thick;
}

.all .width {
  outline-width: 10px;
}
|LiveURL=http://code.webplatform.org/gist/5579241
}}
}}
{{Notes_Section
|Notes=* Displaying an outline does not cause reflow, no matter how wide the outline is. The outline frame is drawn over an element, and does not influence the position or size of the box, or of any other boxes.
* The [[css/properties/outline|outline]] property is a shorthand property for setting one or more of the individual outline properties [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] and [[css/properties/outline-color|outline-color]] in a single rule. In most cases the use of this shortcut is preferable and more convenient.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic User Interface Module Level 3 (CSS3 UI)
|URL=http://dev.w3.org/csswg/css-ui/#outline-width0
|Status=Working Draft
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}