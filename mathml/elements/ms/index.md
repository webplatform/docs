{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''ms''' element represents a string literal meant to be interpreted by programming languages and computer algebra systems.}} By default, string literals are displayed as enclosed by double quotes (&quot;); by using the lquote and rquote attributes, you can set custom characters to display. Note that quotation marks should not be specified unless they are part of the string literal. The content of an <ms> element is not an ASCII string per se, but rather a sequence of characters and [[mathml/elements/mglyph|mglyph]] and [[mathml/elements/malignmark|malignmark]] elements.

{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the ms element:
|Code=<syntaxhighlight lang="html5">
<math>
 
  <ms lquote="„" rquote="“"> abc </ms>
 
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
== Attributes ==
<dl>
<dt id="attr-lquote">
    lquote</dt>
  <dd>
    The opening quote character (depends on <code>dir</code>) to enclose the content. The default value is "<code>&amp;quot;".</code></dd>
 <dt id="attr-mathsize">
    mathsize</dt>
  <dd>
    The size of the content. Possible values are:
* <code>small:</code> Font is rendered smaller than the current font size.
* <code>normal:</code> Equivalent to 100% or 1em.
* <code>big:</code> Font is rendered larger than the current font size.
* or a custom length.
  </dd>
  <dt id="attr-mathvariant">
    mathvariant</dt>
  <dd>
    This logical class of the identifier, which varies in typography. That is, although the names suggest the typographic style for the class, semantically, items with the same class are treated "the same" within an expression, which might or might not involve displaying them with the named typography. The following values are allowed:
* <code>normal</code> (Default value for ''more than one character'')
* <code>bold</code>
* <code>italic</code> (Default value for ''a single character'')
* <code>bold-italic</code>
* <code>double-struck</code>
* <code>bold-fraktur</code>
* <code>script</code>
* <code>bold-script</code>
* <code>fraktur</code>
* <code>sans-serif</code>
* <code>bold-sans-serif</code>
* <code>sans-serif-italic</code>
* <code>sans-serif-bold-italic</code>
* <code>monospace</code>
* <code>initial</code>
* <code>tailed</code>
* <code>looped</code>
* <code>stretched</code>
  </dd>
  <dt id="attr-rquote">
    rquote</dt>
  <dd>
    The closing quote mark (depends on <code>dir</code>) to enclose the content. The default value is "<code>&amp;quot;".</code></dd>
</dl>
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.ms
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
|Opera_supported=Yes
|Opera_version=9.5
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
{{Topics|MathML, Markup_Elements}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/ms
|MSDN_link=
|HTML5Rocks_link=
}}