{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the width of an element.}}
{{CSS Property
|Initial value=auto
|Applies to=All elements except inline, non-replaced elements, table rows, and row groups.
|Inherited=No
|Media=visual
|Animatable=Yes
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Default width of the element, which varies based on the element's type.
* Block-level, non-replaced elements are given a width such that the element's margins, borders, padding, and width add up to the width of the containing element. For example, if the containing element's width is <code>200px</code> and our element has, on both sides, <code>10px</code> margins, <code>1px</code> borders, and <code>5px</code> padding, a width of <code>auto</code> would effectively be 200 - (10 * 2) - (1 * 2) - (5 * 2) = 168px. If any of these conditions were to change, the effective width would change accordingly.
* Inline-block, non-replaced elements are given a "shrink-to-fit" width: the element will be as narrow as the content allows, and no wider than the containing element allows.
* Floating, non-replaced elements are also given a "shrink-to-fit" width.
* Absolutely position, non-replaced elements are like block-level, non-replaced elements, but with the addition of <code>left</code> and <code>right</code> properties: our element's left value, right value, margins, borders, padding, and width will add up to the containing element's width.
* Replaced elements (whether inline, block, inline-block, floating, or absolutely positioned) are tricky because their <code>auto</code> widths are calculated in relation to their heights. If our element has an intrinsic width (for example, an image), and the height is also <code>auto</code>, it maintains its intrinsic width. If our element's height is specified (not <code>auto</code>) and the element has an intrinsic ratio, it will be given a width of (used height) * (intrinsic ratio).

}}{{CSS Property Value
|Data Type=width
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a %. The value is a percentage of the width of the parent object, whether or not it is specified explicitly.  Negative values are not allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This example uses an inline style sheet to set the width of an image.The following examples use the '''width''' attribute and the '''width''' property to change the width of the object.
|Code=&lt;DIV STYLE{{=}}"position:absolute;top:10px;left:10px;width:1in"&gt;
. . . &lt;/DIV&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/width_h.htm
}}{{Single Example
|Language=CSS
|Description=This example uses inline scripting to set the width of an image when an [[dom/events/click|'''onclick''']] event occurs.
|Code=&lt;IMG SRC{{=}}"sphere.jpg" onclick{{=}}"this.style.width{{=}}'1cm'"
    ondblclick{{=}}"this.style.width{{=}}''"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/width_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Microsoft Internet Explorer 6, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property specifies the distance between the left and right edges of the content box—that is, within the [[css/properties/padding|'''padding''']].
When the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, this property includes the object's content box, plus the values of the following properties:  [[css/properties/border-left|'''border-left''']], [[css/properties/border-right|'''border-right''']], [[css/properties/padding-left|'''padding-left''']], and [[css/properties/padding-right|'''padding-right''']].  Subtracting the sum of the values of these properties from the value of the '''width''' property equals the width of the parent object's content box.
To perform operations on the numeric value of this property, use [[css/cssom/properties/pixelWidth|'''pixelWidth''']] or [[css/cssom/properties/posWidth|'''posWidth''']].
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
<code>'''width: '''auto '''{{!}}''' width '''{{!}}''' percentage</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Background, Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>Measuring Element Dimension and Location with CSSOM in Internet Explorer 9</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}