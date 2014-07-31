{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mfrac''' element is used to display fractions.}}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example demonstrates a simple usage of the mfrac element:
|Code=<syntaxhighlight lang="html5">
<math> 
  <mfrac bevelled="true">
     <mfrac>
        <mi> a </mi>
        <mi> b </mi>
     </mfrac>
     <mfrac>
        <mi> c </mi>
        <mi> d </mi>
     </mfrac>
  </mfrac>
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mfrac
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mfrac
|MSDN_link=
|HTML5Rocks_link=
}}
== Attributes ==

<dl>
    <dt id="attr-bevelled">
    bevelled</dt>
  <dd>
    Specifies the way the fraction is displayed. If <code>true</code>, the fraction line is bevelled, which means that numerator and denominator are displayed side by side and separated by a slash (/). Otherwise, if set to <code>false</code> (which is the default value), numerator and denominator are on top of each other.</dd>
 <dt id="attr-denomalign">
    denomalign</dt>
  <dd>
    The alignment of the denominator under the fraction. Possible values are: <code>left</code>, <code>center</code> (default), and <code>right</code>.</dd>
  <dt id="attr-linethickness">
    linethickness</dt>
  <dd>
    The thickness of the horizontal fraction line. The default value is <code>medium</code>, but <code>thin</code>, <code>thick</code>, and other length values can be set.</dd>
  <dt id="attr-numalign">
    numalign</dt>
  <dd>
    The alignment of the numerator over the fraction. Possible values are: <code>left</code>, <code>center</code> (default), and <code>right</code>.</dd>
</dl>