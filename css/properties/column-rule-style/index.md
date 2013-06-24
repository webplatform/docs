{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the style of the rule between columns. The column-rule-style values are the same as for border-style.}}
{{CSS Property
|Initial value=none
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=columnRuleStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. No column rule is drawn, regardless of any specified <code>column-rule-width</code>. The computed value is set to 0.
}}{{CSS Property Value
|Data Type=dotted
|Description=Column rule is a dotted line.
}}{{CSS Property Value
|Data Type=dashed
|Description=Column rule is a dashed line.
}}{{CSS Property Value
|Data Type=solid
|Description=Column rule is a solid line.
}}{{CSS Property Value
|Data Type=double
|Description=Column rule is two parallel solid lines with a space between. The sum of the two single lines and the space between equals the <code>column-rule-width</code> value. The column rule width must be at least 3 pixels wide to draw a double rule.
}}{{CSS Property Value
|Data Type=groove
|Description=3-D groove is drawn in colors slightly lighter and darker than the value. 
}}{{CSS Property Value
|Data Type=ridge
|Description=3-D ridge is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=inset
|Description=3-D inset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=outset
|Description=3-D outset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=hidden
|Description=Same as <code>none</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Uses the <code>column-rule</code> shorthand to set multiple properties at the same time. The <code>column-rule</code> property used is the equivalent of:

<code><pre>column-rule-width: 4px;
column-rule-style: solid;
column-rule-color: green;</pre></code>
|Code=#column3 {
  column-width: 15em;
  column-gap: 2em;

  column-rule: 4px solid green;
  padding: 5px;
}
|LiveURL=http://code.webplatform.org/gist/5305898
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}