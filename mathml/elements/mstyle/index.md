{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Fix broken links
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mstyle''' element is used change the style of its children. It accepts all attributes of all MathML presentation elements with some exceptions and additional attributes listed below.}}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the mstyle element:
|Code=<syntaxhighlight lang="html5">
<math>
 
  <mstyle displaystyle="true" mathcolor="teal">
    <mrow>
     
      <munderover>
        <mo stretchy="true" form="prefix">&sum;</mo>
        <mrow>
          <mi>i</mi>
          <mo form="infix">=</mo>
          <mn>1</mn>
        </mrow>
        <mi>n</mi>
      </munderover>
 
      <mstyle displaystyle="true">
        <mfrac>
          <mn>1</mn>         
          <mi>n</mi>  
        </mfrac>
      </mstyle>
 
    </mrow>
  </mstyle>
 
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mstyle
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
|Opera_supported=No
|Opera_version=
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
{{Topics|MathML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mstyle
|MSDN_link=
|HTML5Rocks_link=
}}
== Attributes ==
<dl>
  <dt id="attr-decimalpoint">
    decimalpoint</dt>
  <dd>
    This attribute is specifying the character for the alignment point within [[mathml/elements/mstack|mstack]] and [[mathml/elements/mtable|mtable]] columns, if the <code>decimalpoint</code> value is used to specify the alignment.</dd>
  <dt id="attr-displaystyle">
    displaystyle</dt>
  <dd>
    A Boolean value specifying whether more vertical space is used for displayed equations or, if set to <code>false</code>, a more compact layout is used to display formulas. The main effect is that larger versions of operators are displayed, when <code>displaystyle</code> is set to <code>true</code>. See also <code>largeop</code> and <code>movablelimits</code> on [[mathml/elements/mo|mo]].</dd>
  <dt id="attr-infixlinebreakstyle">
    infixlinebreakstyle</dt>
  <dd>
    Specifies the default <code>linebreakstyle</code> to use for infix operators. The values <code>before</code>, <code>after</code> and <code>duplicate</code> are allowed.</dd>
  <dt id="attr-scriptlevel">
    scriptlevel</dt>
  <dd>
    Controls mostly the font-size. The higher the <code>scriptlevel</code>, the smaller the font size. This attribute accepts a non-negative integer, as well as a "+" or a "-" sign, which increments or decrements the current value. In addition, the <code>scriptlevel</code> attribute can never reduce the font size below <code>scriptminsize</code> in order to avoid unreadable small font sizes and depends on the multiplier specified in <code>scriptsizemultiplier</code>.</dd>
  <dt id="attr-scriptminsize">
    scriptminsize</dt>
  <dd>
    Specifies a minimum font size allowed due to changes in <code>scriptlevel</code>. The default value is 8pt.</dd>
  <dt id="attr-scriptsizemultiplier">
    scriptsizemultiplier</dt>
  <dd>
    Specifies the multiplier to be used to adjust font size due to changes in <code>scriptlevel</code>. The default value is 0.71.</dd>
</dl>
<p>The <code>&lt;mstyle&gt;</code> element accepts [[mathml/attributes|all attributes]] of all presentation attributes with the following exceptions:</p>
<ul>
  <li><code>height</code>, <code>depth</code> or <code>width</code> do not apply to [[mathml/elements/mglyph|mglyph]], [[mathml/elements/mpadded|mpadded]] or [[mathml/elements/mtable|mtable]].</li>
  <li><code>rowalign</code>, <code>columnalign</code>, or <code>groupalign</code> do not apply to [[mathml/elements/mtr|mtr]], [[mathml/elements/mlabeledtr|mlabeledtr]], [[mathml/elements/mtd|mtd]] or [[mathml/elements/maligngroup|maligngroup]].</li>
  <li><code>lspace</code> or <code>voffset</code> do not apply to [[mathml/elements/mpadded|mpadded]].</li>
  <li><code>fontfamily</code> does not apply to [[mathml/elements/mglyph|mglyph]].</li>
  <li><code>align</code> does not apply to [[mathml/elements/mtable|mtable]] or [[mathml/elements/mstack|mstack]].</li>
  <li><code>index</code> cannot be set on <code>&lt;mstyle&gt;</code>.</li>
  <li><code>src</code> and <code>alt</code> on [[mathml/elements/mglyph|mglyph]] cannot be set on <code>&lt;mstyle&gt;</code>.</li>
  <li><code>actiontype</code> on [[mathml/elements/maction|maction]] cannot be set on <code>&lt;mstyle&gt;</code>.</li>
</ul>