{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The outline-offset property offsets the [[css/properties/outline|outline]] and draw it beyond the border edge.}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=<length> value in absolute units (px or physical).
|Animatable=Yes
|CSS object model property=outlineOffset
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<length>
|Description=Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). For more information about the supported length units, see CSS Values and Units Reference (Length). 
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that the value is inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple &lt;span&gt;s with border and outline.
|Code=&lt;div class="all"&gt;
    &lt;p&gt;
      &lt;span class="one"&gt;One&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="two"&gt;Two&lt;/span&gt;
    &lt;/p&gt;
    &lt;p&gt;
      &lt;span class="three"&gt;Three&lt;/span&gt;
    &lt;/p&gt;
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5579301
}}{{Single Example
|Language=CSS
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
  border: red solid 3px;
  outline: blue solid 3px;
}

.all .one {
  outline-offset: 0px;
}

.all .two {
  outline-offset: 5px;
}

.all .three {
  outline-offset: 0.2em;
}
|LiveURL=http://code.webplatform.org/gist/5579301
}}
}}
{{Notes_Section
|Usage=If the computed value of ‘outline-offset’ is anything other than 0, then the outline is outset from the border edge by that amount.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic User Interface Module Level 3 (CSS3 UI)
|URL=http://dev.w3.org/csswg/css-ui/#outline-offset0
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