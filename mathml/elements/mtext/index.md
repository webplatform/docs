{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mtext''' element is used to render arbitrary text with no notational meaning, such as comments or annotations.
To display text ''with'' notational meaning, use [[mathml/elements/mi|mi]] and [[mathml/elements/mo|mo]] instead.}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the mtext element:
|Code=<syntaxhighlight lang="html5">
<math>
 
  <mtext> Theorem of Pythagoras </mtext> 
 
  <mtext> /* comment here */ </mtext>
   
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
== Attributes ==
<dl>
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
</dl>

{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mtext
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24
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
|Safari_supported=Yes
|Safari_version=5.1
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mtext
|MSDN_link=
|HTML5Rocks_link=
}}