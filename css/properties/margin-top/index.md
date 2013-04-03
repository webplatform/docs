{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Cleanup,Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the top margin of an element.

Margin-top creates space outside the outer edge of an element (beyond the top border). Margins are transparent.
}}
{{CSS Property
|Initial value=0
|Applies to=All elements except elements with table display types other than table-caption, table, and inline-table.
|Inherited=No
|Media=visual
|Computed value=The percentage as specified or the absolute length.
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed width. Negative values are allowed.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage of the width of the containing block. Negative values are allowed. (Even though this is margin-top, the browser will take the percentage from the width, not the height of the containing block.)
}}{{CSS Property Value
|Data Type=auto
|Description=The browser calculates a top margin.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the parent element's specified margin-bottom width.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Clearing the space below an element by 2cm (an example of length).
|Code=margin-top: 2cm;
}}{{Single Example
|Language=CSS
|Description=Clearing the space below an element by 20% of its container's height (an example of percentage).
|Code=margin-top: 20%;
}}{{Single Example
|Language=CSS
|Description=Allowing the browser to decide how much clearance to give an element above its top edge (an example of auto).
|Code=margin-top: auto;
}}{{Single Example
|Language=CSS
|Description=Inheriting the parent element's margin-bottom specification (an example of inherit).
|Code=margin-top: inherit;
}}
}}
{{Notes_Section
|Usage====Usage===
* When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.

===Best Practices===
* When possible, use [http://docs.webplatform.org/wiki/css/properties/margin margin] shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use margin-bottom if there is a specific reason to call attention to it (e.g. one element has a different bottom margin than the rest in its class, etc.).
|Notes====Remarks===
As of Microsoft Internet Explorer 4.0 or later, you can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Internet Explorer 4.0 or later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 or later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements. With earlier versions of Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
For inline elements, the value of this property is used to compute the border area of a surrounding inline element, if present.  This value does not contribute to the height of a line.
Negative margins are supported, except for top and bottom margins on inline objects.

===Standards information===
*[http://www.w3.org/TR/CSS2/box.html#propdef-margin-top w3.org]
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