{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The clip-path property prevents a portion of an element from drawing by defining a clipping region.}}
{{CSS Property
|Initial value=none
|Applies to=All elements. In SVG, applies to container elements (without the <defs> element), all graphics elements, and <clipPath>
|Inherited=No
|Media=visual
|Computed value=As specified, but with <url> values made absolute
|Animatable=Yes
|CSS percentages=As specified
|Values={{CSS Property Value
|Data Type=&lt;basic-shape&gt;
|Description=The following basic shapes can be used to define a clipping region.

* <code>rectangle(<x>, <y>, <width>, <height> [, <rx>, <ry>])</code> Defines the origin and size of the bounding box of the rectangle. Optional arguments '''rx''' and '''ry''' define the x-axis radius and y-axis radius of an ellipse used to round the corners of the rectangle.
* <code>inset-rectangle(<top>, <right>, <bottom>, <left> [, <rx>, <ry>])</code> Defines the origin and size of the bounding box of the inset rectangle. Optional arguments '''rx''' and '''ry''' define the x-axis radius and y-axis radius of an ellipse used to round the corners of the inset rectangle.
* <code>circle(<cx>, <cy>, <r>)</code> Defines a circle by the x and y axes of its center point and its radius.
* <code>ellipse(<cx>, <cy>, <rx>, <ry>)</code> Defines an ellipsis by the x and y axes of its center point and the x and y axes of its radius.
* <code>polygon(<fill-rule>, <x1> <y1>, <x2> <y2>, ..., <xn> <yn>)</code> Defines a polygon based on a filling rule (see [http://www.w3.org/TR/SVG/painting.html#FillRuleProperty SVG fill-rule property] for details) and a list of x and y axes of the polygon's vertices.

See [http://www.w3.org/TR/2013/WD-css-shapes-1-20130620/ CSS Shapes] for more information.
}}{{CSS Property Value
|Data Type=&lt;clip-source&gt;
|Description=The <code><clip-source></code> value may be one of the following.

* <code><url></code> A URL reference to a <code><clipPath></code> element.
* <code>child</code> A keyword to indicate that the last direct child <code><clipPath></code> element of the element to which the <code>clip-path</code> property is applied should be used as the clip source. Equivalent to <code>select(clipPath:last-of-type)</code>.
* <code><child-selector></code> A functional notation accepting a comma-separated list of compound selectors that represents the first matching <code><clipPath></code> element in tree order (as defined in [http://dev.w3.org/fxtf/masking/#DOM DOM]).
}}{{CSS Property Value
|Data Type=none
|Description=No clipping path is created.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following clip-path definition creates a rectangular clip path with rounded corners.
|Code=#image {
    clip-path: rectangle(0%, 0%, 100%, 100%, 20%, 20%); 
}
}}{{Single Example
|Language=CSS
|Description=The following clip-path definition references a <clipPath> element for clipping.
|Code=#image {
    clip-path: url(#clipping); 
}
}}{{Single Example
|Language=HTML
|Description=A <clipPath> element specifies a clipping region. Multiple shapes inside a <clipPath> element result in an additive clipping behavior.

Any shape inside the <clipPath> element and the <clipPath> element itself can be clipped as well. This clipping is exclusive.
|Code=<clipPath id="clipping">
  <circle cx="150" cy="150" r="50" />
  <rect x="150" y="150" width="100" height="100" />
</clipPath>
}}{{Single Example
|Language=CSS
|Description=In this example, the Web Platform Docs logo is clipped in two ways; one shows the icon (clipped with a circle) and the other shows the text (clipped with an ellipse).
|Code=img.clipped-icon {
  /**
   * This clips a circle around the image leaving only the icon visible.
   */
  clip-path: circle(35px, 35px, 30px);
}

img.clipped-text {
  /**
   * This clips the image leaving only the text visible.
   */
  clip-path: ellipse(125px, 40px, 65px, 30px);
}
|LiveURL=http://code.webplatform.org/gist/6338479
}}{{Single Example
|Language=HTML
|Description=The three images that are clipped. The first one (<code>img.original</code>) is the original logo. The second one (<code>img.clipped-icon</code>) is clipped with a circle and the third one (<code>img.clipped-text</code>) is clipped with an ellipse.
|Code=<syntaxhighlight>
<img class="original" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (original)" title="Web Platform Docs logo (original)" />
<img class="clipped-icon" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (icon only)" title="Web Platform Docs logo (icon only)" />
<img class="clipped-text" src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Web Platform Docs logo (text only)" title="Web Platform Docs logo (text only)" />
</syntaxhighlight>
}}
}}
{{Notes_Section}}
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
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic support
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5+
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
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}