{{Page_Title|marquee-style}}
{{Flags
|Checked_Out=No
|Editorial notes=According to W3 specifications, this property should apply to all elements that accept the <code>overflow</code> property. However, it currently only works with the <code>marquee</code> tag. Perhaps this property has been deprecated.
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The 'marquee-style' property determines a marquee's scrolling behavior.}}
{{CSS Property
|Initial value=scroll
|Applies to=non-replaced block-level elements, table cells, and inline-block elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS object model property=marqueeStyle
|Values={{CSS Property Value
|Data Type=scroll
|Description=Start completely off one side, scroll all the way across and completely off.
}}{{CSS Property Value
|Data Type=slide
|Description=Start completely off one side, scroll in, and stop as soon as no more content is off that side.
}}{{CSS Property Value
|Data Type=alternate
|Description=Bounce back and forth.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.scroll { marquee-style: scroll; }
.slide { marquee-style: slide; }
.alternate { marquee-style: alternate; }
|LiveURL=http://code.webplatform.org/gist/6364703
}}{{Single Example
|Language=HTML
|Code=<marquee class="scroll">This demonstrates the 'scroll' value of the 'marquee-style' property.</marquee>
<marquee class="slide">This demonstrates the 'slide' value of the 'marquee-style' property.</marquee>
<marquee class="alternate">This demonstrates the 'alternate' value of the 'marquee-style' property.</marquee>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Marquee Module Level 3
|URL=http://www.w3.org/TR/css3-marquee/
|Status=W3C Candidate Recommendation
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}