{{Flags
|High-level issues=Stub, Copyright Issue
|Content=Outdated, Incomplete, Needs Best Practices
|Compatibility=Missing
|Examples=Examples have errors
}}
{{Summary_Section|The <code>font-size</code> CSS properties specifies the size of the font used for text in the object. Setting the font size may, in turn, change the size of other items, since it is used to compute the value of <code>em</code> and <code>ex</code> length units.}}
{{CSS Property
|Initial value=medium
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=absolute length
|Animatable=Yes
|CSS object model property=fontSize
|CSS percentages=Relative to parent element's font size
|Values={{CSS Property Value
|Data Type=xx-small, x-small, small, medium, large, x-large, xx-large
|Description=A set of absolute size keywords based on the user's default font size (which is medium). Similar to presentational HTML's &lt;font size="1"> through &lt;font size="7"> where the user's default font size is &lt;font size="3">.
}}{{CSS Property Value
|Data Type=larger, smaller
|Description=Larger or smaller than the parent element's font size, by roughly the ratio used to separate the absolute size keywords above.
}}{{CSS Property Value
|Data Type=length
|Description=A positive length. When the units are specified in em or ex,  the size is defined relative to the size of the font on the parent element of the element in question. For example, 0.5em is half the font size of the parent of the current element.
}}{{CSS Property Value
|Data Type=percentage
|Description=A positive percentage of the parent element's font size.
}}
|Syntax=font-size: xx-small
|Value_Name=percentage
}}
{{Examples_Section
|Examples={{Single Example
|Language=CSS
|Description=This is a block of CSS examples.
|Code=/* Set paragraph text to be very large. */
p { font-size: xx-large }
 
/* Set h1 (level 1 heading) text to be 2.5 times the size
 * of the text around it. */
h1 { font-size: 250% }
 
/* Sets text enclosed within span tag to be 16px */
span { font-size: 16px; }
|LiveURL=http://www.google.com
}}{{Single Example
|Language=JavaScript
|Code=var ele = document.getElementyById("my-paragraph");
ele.style.fontSize = "small";
}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://dev.w3.org/csswg/css3-fonts/#font-size-prop
|Status=Working Draft
|Relevant_changes=No change
}}{{Related Specification
|Name=CSS Transitions
|URL=http://dev.w3.org/csswg/css3-transitions/#animatable-css
|Status=Working Draft
|Relevant_changes=Defines <code>font-size</code> as animatable
}}{{Related Specification
|Name=CSS 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/fonts.html#propdef-font-size
|Status=Recommendation
|Relevant_changes=No change
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#font-size
|Status=Recommendation
|Relevant_changes=Original specification
}}
}}
{{Compatibility_Section
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome=5.0
|Chrome_prefixed=4.0
|Firefox=1.0
|Internet_explorer=7.0
|Opera=1.0
|Safari={{Compat_Supported}}
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic Support
|Android=1.0
|Firefox_mobile=1.0
|IE_phone=6.0
|Opera_mobile=6.0
|Safari_mobile=1.0
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6+
|Note=When using the <code>!DOCTYPE</code> declaration to specify standards-compliant mode, the default value for this property is <code>medium</code>, not <code>small</code>.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=4+
|Note=Possible length values specified in a relative measurement, using the height of the element's font (em) or the height of the letter "x" (ex)
}}
}}
{{Editorial/Copyright Issue | Some content is under CC-BY-SA, but we haven't wrapped which pieces. }}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/font-size
|HTML5Rocks_link=
}}