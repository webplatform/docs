{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>text-justify</code> CSS property offers a fine level of justification control over the enclosed content, allowing for a variety of sophisticated justification models used in different language writing systems.}}
{{CSS Property
|Initial value=auto
|Applies to=block containers and, optionally, inline elements
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=textJustify
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Allows the browser to determine which justification algorithm to apply.
}}{{CSS Property Value
|Data Type=none
}}{{CSS Property Value
|Data Type=inter-word
|Description=Aligns text by increasing the space between words. This value's spacing behavior is the fastest way to make all lines of text equal in length. Its justification behavior does not affect the last line of the paragraph.
}}{{CSS Property Value
|Data Type=inter-ideograph
|Description=Justifies lines of ideographic text, and increases or decreases both inter-ideograph and inter-word spacing.
}}{{CSS Property Value
|Data Type=inter-cluster
|Description=Justifies lines of text that contain no inter-word spacing. This form of justification is optimized for documents in Asian languages.
}}{{CSS Property Value
|Data Type=distribute
|Description=Handles spacing much like the '''newspaper''' value. This form of justification is optimized for documents in Asian languages, such as Thai.
}}{{CSS Property Value
|Data Type=kashida
|Description=Justifies lines of text by elongating characters at chosen points.  This form of justification is intended for Arabic script languages.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''-ms-text-justify''' attribute and the '''-ms-text-justify''' property to align text within the object.
|Code=...
&lt;DIV style{{=}}"text-align:justify; text-justify:distribute-all-lines;"&gt;
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
    This is something. This example demonstrates how to this 
    property. This is something. This example demonstrates how to use this
    property. This is something. This example demonstrates how to
    use this property. This is something. This example demonstrates
    how to use this property. This is something. This example
    demonstrates how to use this property. This is something.
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
&lt;/DIV&gt;                
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-justify.htm
}}{{Single Example
|Description=This example uses inline scripting to change the alignment of the text when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=...
&lt;DIV style{{=}}"cursor:hand; text-align:justify;"
    onmouseover{{=}}"this.style.textJustify{{=}}'distribute-all-lines';"
    onmouseout{{=}}"this.style.textJustify{{=}}'auto';"&gt;
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
    This is something. This example demonstrates how to this 
    property. This is something. This example demonstrates how to use this
    property. This is something. This example demonstrates how to
    use this property. This is something. This example demonstrates
    how to use this property. This is something. This example
    demonstrates how to use this property. This is something.
    This example demonstrates how to use this property. This is
    something. This example demonstrates how to use this property.
&lt;/DIV&gt;                
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textJustify.htm
}}
}}
{{Notes_Section
|Usage=Enables proper alignment of various languages such as chinese.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#text-justify0
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.0 +
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=8.0 +
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
|Topic_clusters=CSS Layout, Text
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Manual_sections=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
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