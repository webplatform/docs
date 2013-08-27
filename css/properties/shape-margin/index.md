{{Page_Title}}
{{Flags
|Content=Examples Needed
|Checked_Out=No
|Editorial notes=It seems like wrap-margin has been renamed to shape-margin. See this: http://www.w3.org/TR/css3-exclusions/#wrap-margin channel log:

Since May 3rd 2012: "Changed wrap-margin and wrap-padding to shape-margin and shape-padding."

And this seems to be the new specs: http://www.w3.org/TR/2013/WD-css-shapes-1-20130620/#shape-margin-property
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Set the value that is used to offset the inner wrap shape from other shapes. Inline content that intersects a shape with this property will be pushed by this shape's margin.}}
{{CSS Property
|Initial value=0
|Applies to=exclusion elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=<length>
|Description=The value that is used to offset the inner wrap shape from other shapes.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, we have an image with a CSS class and a paragraph wrapped in a P tag.
|Code=&lt;p&gt;
  &lt;img class=&quot;logo&quot; src=&quot;http://docs.webplatform.org/w/skins/webplatform/images/logo.png&quot;/&gt;

  We are an open community of developers building resources for a better web, regardless of brand, browser or platform. Anyone can contribute and each person who does makes us stronger. Together we can continue to drive innovation on the Web to serve the greater good. It starts here, with you.
&lt;/p&gt;
}}{{Single Example
|Language=CSS
|Description=In the CSS class, we float the image left, set its shape to be the same image, and then we set a margin of 16px.
|Code=.logo {
    float  : left;
    shape-outside : url("http://docs.webplatform.org/w/skins/webplatform/images/logo.png");
    shape-margin : 16px;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Uses a vendor prefixed version of an old name of this property - wrap-margin.
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=25.0.1364.160
|Note=Using vendor prefix -webkit-
}}{{Compatibility Notes Row
|Browser=Opera
|Version=12.14
|Note=Using vendor prefix -o- 
}}{{Compatibility Notes Row
|Browser=FireFox
|Version=19
|Note=Using vendor prefix -moz-
}}{{Compatibility Notes Row
|Browser=Safari
|Version=534.57.2
|Note=Using vendor prefix -webkit-
}}
}}
{{See_Also_Section
|Manual_links=See also: [[css/properties/wrap-flow|wrap-flow]] property
}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/windows/apps/hh466103.aspx
|HTML5Rocks_link=
}}