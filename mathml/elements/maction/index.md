{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs review
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''maction''' element provides a possibility to bind actions to (sub-) expressions.
The action itself is specified by the actiontype attribute, which accepts several values. To specify which child elements are addressed by the action, you can make use of the selection attribute.
}}
{{Markup_Element}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of maction:
|Code=<syntaxhighlight lang="html5"><math>
 
<maction actiontype="toggle">
 
  <mfrac>
    <mn>6</mn>
    <mn>8</mn>
  </mfrac>
   
  <mfrac>
    <mrow>
      <mn>3</mn>
      <mo>&sdot;</mo>
      <mn>2</mn>
    </mrow>
    <mrow>
      <mn>4</mn>
      <mo>&sdot;</mo>
      <mn>2</mn>
    </mrow>   
  </mfrac>
 
  <mfrac>
    <mn>3</mn>
    <mn>4</mn>
  </mfrac>
 
</maction>
 
</math></syntaxhighlight>
}}
}}
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
|Chrome_supported=No
|Chrome_version=
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/maction
|MSDN_link=
|HTML5Rocks_link=
}}
== Attributes == 
<dl>
  <dt>
    actiontype</dt>
  <dd>
    The action which specifies what happens for this element. Possible values are:
* '''statusline''': If there is a click on the ''expression'' or the reader moves the pointer over it, the ''message'' is sent to the browser's status line. The syntax is: &lt;maction actiontype="statusline"&gt; ''expression'' ''message'' &lt;/maction&gt;.

* '''toggle''': When there is a click on the subexpression, the rendering alternates the display of selected subexpressions. Therefore each click increments the '''selection''' value.<br />
        The syntax is: &lt;maction actiontype="toggle" selection="''positive-integer''" &gt; ''expression1 expression2 expressionN'' &lt;/maction&gt;.

* '''tooltip''': When the pointer moves over the ''expression'', a tooltip box with a ''message'' is displayed near the expression.<br />
        The syntax is: &lt;maction actiontype="tooltip"&gt; <em>expression</em> ''message'' &lt;/maction&gt;.
  </dd>
  <dt id="attr-selection">
    selection</dt>
  <dd>
    The child element which is addressed by the action. The default value is ''1'' which is the first child element.</dd>
</dl>