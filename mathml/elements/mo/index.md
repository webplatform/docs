{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mo''' element represents an operator in a broad sense. Besides operators in strict mathematical meaning, this element also includes "operators" like parentheses, separators like comma and semicolon, or "absolute value" bars.}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the mo element:
|Code=<syntaxhighlight lang="html5">
<math>
 
<mrow>
  <mn>5</mn>
  <mo>+</mo>
  <mn>5</mn>
</mrow>
 
<mrow>
  <mo> [ </mo> <!-- default form value: prefix -->
  <mrow>
    <mn> 0 </mn>
    <mo> ; </mo> <!-- default form value: infix -->
    <mn> 1 </mn>
  </mrow>
  <mo> ) </mo> <!-- default form value: postfix -->
</mrow>
 
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
== Attributes ==
<dl>
<dt id="attr-accent">
    accent</dt>
  <dd>
    If the operator is used as an [[mathml/elements/munder|under]]- or [[mathml/elements/mover|overscript]] this attribute specifies whether the operator should be treated as an accent.<br />
    Allowed values are <code>true</code> or <code>false</code>.</dd>
<dt id="attr-fence">
    fence</dt>
  <dd>
    There is no visual effect for this attribute, but it specifies whether the operator is a fence (such as parentheses).<br />
    Allowed values are <code>true</code> or <code>false</code>.</dd>
  <dt id="attr-form">
    form</dt>
  <dd>
    Specifies the role of the operator in an enclosed expression, which affects spacing and other default properties. For ordinary operators (+, -, etc. ) you usually do not need to specify this attribute explicitly.<br />
    Possible values are:
* <code>prefix</code>, for opening fences. (It is the default value if the operator is the first argument in a [[mathml/elements/mrow|mrow]] element with more than one argument.)
* <code>infix</code>, for separators. (It is the default value if the operator is not included in a [[mathml/elements/mrow|mrow]] element.)
* <code>postfix</code>, closing fences. (It is the default value if the operator is the last argument in a [[mathml/elements/mrow|mrow]] element with more than one argument.)
  </dd>
 <dt id="attr-largeop">
    largeop</dt>
  <dd>
    Specifies whether the operator should be drawn larger than normal when <code>displaystyle="true"</code> is set. Allowed values are either <code>true</code> or <code>false</code>.</dd>
  <dt id="attr-lspace">
    lspace</dt>
  <dd>
    The amount of space before the operator (see length for values and units). The constant <code>thickmathspace</code> (5/18em) is the default value.</dd>
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
<dt id="attr-maxsize">
    maxsize</dt>
  <dd>
    If <strong>stretchy</strong> is <code>true</code>, this attribute specifies the maximum size of the operator. Allowed values are:
* <code>infinity</code>
* an arbitrary length
  </dd>
  <dt id="attr-minsize">
    minsize</dt>
  <dd>
    If <strong>stretchy</strong> is <code>true</code>, this attribute specifies the minimum size of the operator. Allowed values are:
* <code>infinity</code>
* an arbitrary length
  </dd>
  <dt id="attr-movablelimits">
    movablelimits</dt>
  <dd>
    Specifies whether attached under- and overscripts move to sub- and superscript positions when <strong>displaystyle</strong> is <code>false</code>.<br />
    Allowed values are either <code>true</code> or <code>false.</code></dd>
  <dt id="attr-rspace">
    rspace</dt>
  <dd>
    The amount of space after the operator (see length for values and units). The constant <code>thickmathspace</code> (5/18em) is the default value.</dd>
  <dt id="attr-separator">
    separator</dt>
  <dd>
    There is no visual effect for this attribute, but it specifies whether the operator is a separator (such as commas).<br />
    Allowed values are <code>true</code> or <code>false</code>.</dd>
  <dt id="attr-stretchy">
    stretchy</dt>
  <dd>
    Specifies whether the operator stretches to the size of the adjacent element.<br />
    Allowed values are <code>true</code> or <code>false</code>.</dd>
  <dt id="attr-symmetric">
    symmetric</dt>
  <dd>
    If <strong>stretchy</strong> is <code>true</code>, this attribute specifies whether the operator should be vertically symmetric around the imaginary math axis (centered fraction line).<br />
    The default value is <code>true</code> if <strong>stretchy</strong> is set to <code>true</code> and otherwise <code>false</code>. Allowed values are <code>true</code> or <code>false</code>.</dd>
</dl>
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mo
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mo
|MSDN_link=
|HTML5Rocks_link=
}}