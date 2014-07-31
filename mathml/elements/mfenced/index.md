{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mfenced''' element provides the possibility to add custom opening and closing parentheses (such as brackets) and separators (such as commas or semicolons) to an expression. }}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=These examples demonstrate a simple usage of the mfenced element:
|Code=<syntaxhighlight lang="html5">
<math>
  <mfenced open="{" close="}" separators=";;,">
    <mi>a</mi>
    <mi>b</mi>
    <mi>c</mi>
    <mi>d</mi>
    <mi>e</mi>
  </mfenced>
</math>

<math>
  <mfenced open="[" close="]" separators="||||,">
    <mi>a</mi>
    <mi>b</mi>
    <mi>c</mi>
    <mi>d</mi>
    <mi>e</mi>
  </mfenced>
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}

== Attributes ==

<dl>
  <dt id="attr-close">close</dt>
  <dd> A string for the closing delimiter. The default value is ")" and any white space is trimmed.</dd>
<dt id="attr-open">
    open</dt>
  <dd>
    A string for the opening delimiter. The default value is <code>"("</code> and any white space is trimmed.</dd>
  <dt id="attr-separators">
    separators</dt>
  <dd>
    A sequence of zero or more characters to be used for different separators, optionally divided by white space, which is ignored. The default value is ",". By specifying more than one character, it is possible to set different separators for each argument in the expression. If there are too many separators, all excess is ignored. If there are too few separators in the expression, the last specified separator is repeated.</dd>
</dl>
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mfenced
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
|Firefox_version=1
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mfenced
|MSDN_link=
|HTML5Rocks_link=
}}