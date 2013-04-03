{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Cleanup, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the left margin of an element.

Margin-bottom clears an area below an element (outside the border). The margin does not have a background color, and is completely transparent.
}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length.
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed width. Negative values are allowed.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage of the width of the containing block. Negative values are allowed.
}}{{CSS Property Value
|Data Type=auto
|Description=The browser calculates a bottom margin.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the parent element's specified margin-bottom width.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Clearing the space to the left of an element by 2cm (an example of length).
|Code=margin-left: 2cm;
}}{{Single Example
|Language=CSS
|Description=Clearing the space to the left of an element by 20% of its container's width (an example of percentage).
|Code=margin-left: 20%;
}}{{Single Example
|Language=CSS
|Description=Allowing the browser to decide how much clearance to give an element to the left of its left edge (an example of auto).
|Code=margin-left: auto;
}}{{Single Example
|Language=CSS
|Description=Inheriting the parent element's margin-left specification (an example of inherit).
|Code=margin-left: inherit;
}}
}}
{{Notes_Section
|Usage====Syntax===
id, class, or html element {

    margin-left: value;
}

===Usage===
* When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.

===Best Practices===
* When possible, use [http://docs.webplatform.org/wiki/css/properties/margin margin] shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use margin-bottom if there is a specific reason to call attention to it (e.g. one element has a different left margin than the rest in its class, etc.).
|Notes====Remarks===
You can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
This property applies to inline elements, starting with Microsoft Internet Explorer 5.5.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Negative margins are supported, except for top and bottom margins on inline objects.

===Standards Information===
[http://www.w3.org/TR/CSS2/box.html#propdef-margin-left w3.org]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=All
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=All
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=All
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=All
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=All
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=All
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=All
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=All
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=All
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=All
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=All
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=All
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=All
|Safari_mobile_prefixed_supported=Unknown
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}