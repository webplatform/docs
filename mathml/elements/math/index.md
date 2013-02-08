{{Page_Title|The toplevel MathML element}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The top-level element in MathML is '''<math>'''. Every valid MathML instance must be wrapped in <math> tags. In addition you must not nest a second <math> element in another, but you can have an arbitrary number of other child elements in it.}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a simple formula written in MathML
|Code=<syntaxhighlight lang="html5"><!DOCTYPE html>
<html>
  <head>
    <title>MathML in HTML5</title>
  </head>
  <body>
 
  <math>
    <mrow>
      <mrow>
        <msup>
          <mi>a</mi>
          <mn>2</mn>
        </msup>
        <mo>+</mo>
        <msup>
          <mi>b</mi>
          <mn>2</mn>
        </msup>
      </mrow>
      <mo>=</mo>
      <msup>
        <mi>c</mi>
        <mn>2</mn>
      </msup>
    </mrow>
  </math>
 
  </body>
</html> </syntaxhighlight>
}}
}}
== Attributes == 
In addition to the following attributes, the  '''math''' element accepts any attributes of the [[mathml/elements/mstyle|mstyle]] element.
<dl>
  <dt id="attr-display">display</dt>
  <dd>
    This enumerated attribute specifies how the enclosed MathML markup should be rendered. It can have one of the following values:
      
* '''block''', which means that this element will be displayed outside the current span of text, as a block that can be positioned anywhere without changing the meaning of the text;
* '''inline''', which means that this element will be displayed inside the current span of text, and cannot be moved out of it without changing the meaning of that text.

  </dd>
  <dt>
    mode '''(depreacted)'''</dt>
  <dd>
    Deprecated in favor of the display attribute.<br />
    Possible values are: '''display''' (which has the same effect as display="block") and '''inline'''.</dd>
</dl>
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0 
|URL=http://www.w3.org/TR/MathML3/chapter2.html#interf.toplevel
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24
|Chrome_prefixed_supported=
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
|Opera_mini_supported=
|Opera_mini_version=Unknown
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
}}
{{Topics|MathML, Markup_Elements}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/math
|MSDN_link=
|HTML5Rocks_link=
}}