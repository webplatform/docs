{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''menclose''' element renders its content inside an enclosing notation specified by the notation attribute.}}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a simple markup using menclose:
|Code=<syntaxhighlight lang="html5"><math>
  <menclose notation="circle box">
    <mi> x </mi>
    <mo> + </mo>
    <mi> y </mi>
  </menclose>
</math></syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.menclose
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
{{Topics|MathML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/menlose
|MSDN_link=
|HTML5Rocks_link=
}}
== Attributes == 
<dl>
  <dt>notation</dt>
  <dd> Multiple values are possible:
 <table>
        <tr>
          <th>Value</th>
          <th>Description</th>
        </tr>
        <tr>
          <td>longdiv (default)</td>
          <td>long division symbol</td>
        </tr>
        <tr>
          <td>actuarial</td>
          <td>[http://en.wikipedia.org/wiki/Actuarial_notation actuarial symbol]</td>
        </tr>
        <tr>
          <td>radical</td>
          <td>square root symbol</td>
        </tr>
        <tr>
          <td>box</td>
          <td>box</td>
        </tr>
        <tr>
          <td>roundedbox</td>
          <td>rounded box</td>
        </tr>
        <tr>
          <td>circle</td>
          <td>circle</td>
        </tr>
        <tr>
          <td>left</td>
          <td>line to the left of the contents</td>
        </tr>
        <tr>
          <td>right</td>
          <td>line to the right of the contents</td>
        </tr>
        <tr>
          <td>top</td>
          <td>line above of the contents</td>
        </tr>
        <tr>
          <td>bottom</td>
          <td>line below of the contents</td>
        </tr>
        <tr>
          <td>updiagonalstrike</td>
          <td>strikeout line through contents from lower left to upper right</td>
        </tr>
        <tr>
          <td>downdiagonalstrike</td>
          <td>strikeout line through contents from upper left to lower right</td>
        </tr>
        <tr>
          <td>verticalstrike</td>
          <td>vertical strikeout line through contents</td>
        </tr>
        <tr>
          <td>horizontalstrike</td>
          <td>horizontal strikeout line through contents</td>
        </tr>
        <tr>
          <td>madruwb</td>
          <td>[http://en.wikipedia.org/wiki/Modern_Arabic_mathematical_notation Arabic factorial symbol]</td>
        </tr>
    </table>
  </dd>
</dl>