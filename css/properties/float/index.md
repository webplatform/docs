{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Elements which have the style <code>float</code>  are floated horizontally.  These elements can move as far to the <code> left</code> or <code>right</code>  of the containing element.  All elements after the floating element will flow around it, but elements before the floating element are not impacted.  If several floating elements are placed after each other, they will float next to each other as long as there is room.}}
{{CSS Property
|Initial value=none
|Applies to=all elements except absolutely positioned, replaced elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=<code>none</code> indicates that the element does not contain any float at all. This is the initial value of the <code>float</code> property.
}}{{CSS Property Value
|Data Type=left
|Description=The <code>left</code> value indicates that the element must float to the far left side of its containing block.
}}{{CSS Property Value
|Data Type=right
|Description=The <code>right</code> value indicates that the element must float to the far right side of its containing block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In this example, we create a simple layout containing a title, a logo (image) and some textual content. Notice the use of the <code>clearfix</code> class on the <code>article</code> element below.
|Code=&lt;article class="clearfix"&gt;
  &lt;img class="logo" src="http://www.webplatform.org/logo/wplogo_pillow_tan.png" alt="Web Platform Docs logo" /&gt;
  &lt;h1&gt;Web Platform Docs&lt;/h1&gt;
  &lt;p class="desc"&gt;Web Platform Docs is a community-driven site that aims to become a comprehensive and authoritative source for web developer documentation. Learn more about &lt;a href="http://docs.webplatform.org"&gt;Web Platform Docs&lt;/a&gt;. To understand the &lt;a href="http://docs.webplatform.org/wiki/css/properties/float"&gt;&lt;code&gt;float&lt;/code&gt;&lt;/a&gt; and the &lt;a href="https://developer.mozilla.org/en-US/docs/Web/CSS/float#Clearing_floats"&gt;&lt;code&gt;clear&lt;/code&gt;&lt;/a&gt; property.&lt;/p&gt;
  &lt;/div&gt;
&lt;/article&gt;
|LiveURL=http://code.webplatform.org/gist/5974883
}}{{Single Example
|Language=CSS
|Description=The CSS for the above layout is described below. Notice the use of the <code>float</code>s.
|Code=/* Some CSS rules remove for brevity; please see the live URL for the complete example. */

.logo {
  float: left;
}

.desc {
  float: left;
  width: 60%;
}
|LiveURL=http://code.webplatform.org/gist/5974883
}}
}}
{{Notes_Section
|Usage=As float implicitly implies the use of the block layout, it modifies the computed value of the [[css/properties/display|display]] values in some cases:


{{{!}}
{{!}}-
! Specified value !! Computed value
{{!}}-
{{!}} inline {{!}}{{!}} block
{{!}}-
{{!}} inline-block {{!}}{{!}} block
{{!}}-
{{!}} inline-table {{!}}{{!}} table
{{!}}-
{{!}} table-row {{!}}{{!}} block
{{!}}-
{{!}} table-row-group {{!}}{{!}} block
{{!}}-
{{!}} table-column {{!}}{{!}} block
{{!}}-
{{!}} table-column-group {{!}}{{!}} block
{{!}}-
{{!}} table-cell {{!}}{{!}} block
{{!}}-
{{!}} table-caption {{!}}{{!}} block
{{!}}-
{{!}} table-header-group {{!}}{{!}} block
{{!}}-
{{!}} table-footer-group {{!}}{{!}} block
{{!}}-
{{!}} flex {{!}}{{!}} flex, but float has no effect on such elements
{{!}}-
{{!}} inline-flex {{!}}{{!}} inline-flex, but float has no effect on such elements
{{!}}-
{{!}} other {{!}}{{!}} unchanged
{{!}}}

'''Note:''' If you're referring to this property from JavaScript as a member of the element.style object, you must spell it as cssFloat. Also note that Internet Explorer versions 8 and older spelled this styleFloat. This is an exception to the rule that the name of the DOM member is the camel-case name of the dash-separated CSS name (and is due to the fact that "float" is a reserved word in JavaScript, as with the need to escape "class" as "className" and escape <label>'s "for" as "htmlFor").
|Notes====Remarks===
* When using floats it's often necessary to clear the parent element. Check out the [[css/properties/clear|clear]]-property.
* Objects following a floating object move in relation to the position of the floating object.
* The floating object is moved left or right until it reaches the border, padding, or margin of another block-level object.
|Import_Notes====Syntax===
<code>'''float: '''left '''{{!}}''' right '''{{!}}''' none '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.25
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/#floating0
|Status=Working Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/visuren.html#float-position
|Status=Recommendation
|Relevant_changes=No change.
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#float
|Status=Recommendation
|Relevant_changes=Initial definition.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/float
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}