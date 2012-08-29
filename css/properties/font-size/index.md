{{Flags
|High-level issues=Stub, Copyright Issue
|Content=Outdated, Incomplete, Needs Best Practices
|Compatibility=Missing
|Examples=Examples have errors
|Editorial notes={{Editorial/Copyright Issue | Some content is under CC-BY-SA, but we haven't wrapped which pieces. }}
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
{{Notes_Section
|Usage=There are several ways to specify the font size, with keywords or numerical values for pixels or ems. Choose the appropriate method based on the needs for the particular web page.

===Keywords===

Keywords are a good way to set the size of fonts on the web. By setting a keyword font size on the body element, you can set relative font-sizing everywhere else on the page, giving you the ability to easily scale the font up or down on the entire page accordingly.
Pixels

Setting the font size in pixel values (<code>px</code>) is a good choice when you need pixel accuracy. A <code>px</code> value is static. This is an OS-independent and cross-browser way of literally telling the browsers to render the letters at exactly the number of pixels in height that you specified. The results may vary slightly across browsers, as they may use different algorithms to achieve a similar effect.

Font sizing settings can also be used in combination. For example, if a parent element is set to <code>16px</code> and its child element is set to <code>larger</code>, the child element displays larger than the parent element in the page.

{{Note|Defining font sizes in pixel is ''not accessible'', because the user cannot change the font size from the browser. (For example, users with limited vision may wish to set the font size much larger than the size chosen by a web designer.) Therefore, avoid using pixels for font sizes if you wish to create an inclusive design.}}


===Ems===

Another way of setting the font size is with <code>em</code> values. The size of an <code>em</code> value is dynamic. When defining the <code>font-size</code> property, an <code>em</code> is equal to the size of the font that applies to the parent of the element in question. If you haven't set the font size anywhere on the page, then it is the browser default, which is probably 16px. So, by default 1em = 16px, and 2em = 32px. If you set a font-size of 20px on the body element, then 1em = 20px and 2em = 40px. Note that the value 2 is essentially a multiplier of the current <code>em</code> size.

In order to calculate the <code>em</code> equivalent for any pixel value required, you can use this formula:

{{Inline_Example|Code=em = desired element pixel value / parent element font-size in pixels|Language=CSS}}

For example, suppose the font-size of the body of the page is set to 1em, with the browser standard of 1em = 16px; if the font-size you want is 12px, then you should specify 0.75em (because 12/16 = 0.75). Similarly, if you want a font size of 10px, then specify 0.625em (10/16 = 0.625); for 22px, specify 1.375em (22/16).

A popular technique to use throughout the document is to set the the font-size of the body to 62.5% (that is 62.5% of the default of 16px), which equates to 10px, or 0.625em. Now you can set the font-size for any elements using em units, with an easy-to-remember conversion, by dividing the px value by 10. This way 6px = 0.6em, 8px = 0.8em, 12px = 1.2em, 14px = 1.4em, 16px = 1.6em. For example:

{[Inline_Example|Code=body {
  font-size: 62.5%; /* font-size 1em = 10px */
}
p {
  font-size: 1.6em; /* 1.6em = 16px */
}|Language=CSS}}

The em is a very useful unit in CSS, since it can adapt automatically to the font that the reader chooses to use.
|Notes=The <code>em</code> and <code>ex</code> units on the font-size property are relative to the parent element's font size (unlike all other properties, where they're relative to the font size on the element). This means em units and percentages do the same thing for font-size.
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
{{See_Also_Section
|Content====Related CSS Properties===
* <code>[[CSS/properties/font | font]]</code>
* <code>[[CSS/properties/font-family | font-family]]</code>
* <code>[[CSS/properties/font-size | font-size]]</code>
* <code>[[CSS/properties/font-size-adjust | font-size-adjust]]</code>
* <code>[[CSS/properties/font-stretch | font-stretch]]</code>
* <code>[[CSS/properties/font-style | font-style]]</code>
* <code>[[CSS/properties/font-variant | font-variant]]</code>
* <code>[[CSS/properties/font-weight | font-weight]]</code>

===Related CSS At Rules===
* <code>[[CSS/atrules/@font-face | @font-face]]</code>

===Related DOM Interfaces===
* <code>[[DOM/element/CSSStyleDeclaration | CSSStyleDeclaration]]</code>

===Related DOM properties===
* <code>[[DOM/element/properties/currentStyle | element.currentStyle]]</code>
* <code>[[DOM/element/properties/defaults | element.defaults]]</code> ''IE Only''
}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/font-size
|HTML5Rocks_link=
}}