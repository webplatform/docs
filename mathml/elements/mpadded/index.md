{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mpadded''' element is used to add extra padding and to set the general adjustment of position and size of enclosed contents.}}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the mpadded element:
|Code=<syntaxhighlight lang="html5">
<math>
 
  <mpadded height="+150px" width="100px" lspace="2height">
    <mi> x </mi>
    <mo> + </mo>
    <mi> y </mi>
  </mpadded>
 
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mpadded
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|MathML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mpadded
|MSDN_link=
|HTML5Rocks_link=
}}
== Attributes ==
<dl>
  <dt id="attr-depth">
    depth</dt>
  <dd>
    Sets or increments the depth. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .</dd>
  <dt id="attr-height">
    height</dt>
  <dd>
    Sets or increments the height. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .</dd>
  <dt id="attr-lspace">
    lspace</dt>
  <dd>
    Sets or increments the horizontal position. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .</dd>
  <dt id="attr-voffset">
    voffset</dt>
  <dd>
    Sets or increments the vertical position. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .</dd>
  <dt id="attr-width">
    width</dt>
  <dd>
    Sets or increments the width. Possible values: Any length or an increment/decrement (a length prefixed with "+" or "-") .</dd>
</dl>
=== Pseudo-units ===
It is possible to use the keywords <code>"depth</code>",<code> "height"</code>, and <code>"width"</code> as a pseudo-unit for the attributes <code>depth</code>, <code>height</code>, <code>lspace</code>, <code>voffset</code>, and <code>width</code>. They represent each length of the same-named dimension.