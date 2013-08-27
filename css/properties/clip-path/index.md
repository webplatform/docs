{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The clip-path property prevents portion of elements from drawing by a defined clipping region.}}
{{CSS Property
|Initial value=none
|Applies to=All elements. SVG container elements, graphics elements and ‘clipPath’
|Inherited=No
|Media=visual
|Computed value=as specified, but with <url> values made absolute
|Animatable=Yes
|CSS percentages=as specified
|Values={{CSS Property Value
|Data Type=&lt;shape&gt;
|Description=The following basic shapes can be used to define a clipping region:

* <code>rectangle(&lt;x&gt;, &lt;y&gt;, &lt;width&gt;, &lt;height&gt; [, &lt;rx&gt;, &lt;ry&gt;])</code> defines a rectangle with an origin and a size. The optional arguments '''rx''' and '''ry''' define the "rounded corners" in the horizontal and vertical direction.
* <code>inset-rectangle(&lt;top&gt;, &lt;right&gt;, &lt;bottom&gt;, &lt;left&gt; [, &lt;rx&gt;, &lt;ry&gt;])</code> defines a rectangle by top, right, bottom and left insets. The optional arguments '''rx''' and '''ry''' define the "rounded corners" in the horizontal and vertical direction.
* <code>circle(<cx, <cy>, <r>)</code> defines a circle with a center point and a radius.
* <code>ellipse(<cx, <cy>, <rx>, <ry>)</code> defines a circle with a center point and a radii for the horizontal and vertical directions.
* <code>polygon(<x1> <y1>, <x2> <y2>, ..., <xn> <yn>)</code> defines a polygon based on a list of points
}}{{CSS Property Value
|Data Type=&lt;url&gt;
|Description=URL reference to a &lt;clipPath&gt; element.
}}{{CSS Property Value
|Data Type=none
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following clip-path definition creates a rectangular clip path with "rounded corners".
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
|Language=Other
|Description=A <clipPath> element specifies a clipping region. Multiple shapes inside a <clipPath> element result in an additive clipping behavior.

Any shape inside the <clipPath> element and the <clipPath> element itself can be clipped as well. This clipping is exclusive.
|Code=<syntaxhighlight>
  <clipPath id="clipping">
    <circle cx="150" cy="150" r="50" />
    <rect x="150" y="150" width="100" height="100" />
  </clipPath>
</syntaxhighlight>
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
|URL=http://dvcs.w3.org/hg/FXTF/raw-file/tip/masking/index.html
|Status=Editor's Draft
}}{{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/SVG/
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
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
{{See_Also_Section
|Topic_clusters=Visual Effects
}}
{{Topics|CSS, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}