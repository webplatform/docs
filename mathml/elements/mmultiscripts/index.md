{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The MathML '''mmultiscripts''' element allows you to create tensor-like objects.}}
{{Markup_Element
|DOM_interface=mathml
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=These examples demonstrate a simple usage of the mmultiscripts element:
|Code=<syntaxhighlight lang="html5">
<math> 
 
    <mmultiscripts>
 
        <mi>X</mi>      <!-- base expression --> 
 
        <mi>d</mi>      <!-- postsubscript -->
        <mi>c</mi>      <!-- postsuperscript -->
 
        <mprescripts />
        <mi>b</mi>      <!-- presubscript -->
        <mi>a</mi>      <!-- presuperscript -->
 
    </mmultiscripts>
 
</math>

<math> 
 
    <mmultiscripts>
 
        <mi>X</mi>      <!-- base expression -->
 
        <none />        <!-- postsubscript -->
        <mi>c</mi>      <!-- postsuperscript -->
 
        <mprescripts />
        <mi>b</mi>      <!-- presubscript -->
        <none />        <!-- presuperscript -->
 
    </mmultiscripts>
 
</math>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=MathML 3.0
|URL=http://www.w3.org/TR/MathML3/chapter3.html#presm.mmultiscripts
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
|MDN_link=https://developer.mozilla.org/en-US/docs/MathML/Element/mmultiscripts
|MSDN_link=
|HTML5Rocks_link=
}}
In a descriptive way [http://en.wikipedia.org/wiki/Tensor tensors] are multidimensional matrices (mathematical imprecise but exemplified). The degree of a tensor depends on the dimensionality of a representative array. For example, a number is a 0-dimensional array, or a 0th-order tensor. A 1-dimensional array (e.g. vectors) is a 1st-order tensor and so 2nd-order tensors are needed to represent square matrices. To learn more about the mathematical background of tensors refer to the [http://en.wikipedia.org/wiki/Tensor entry on Wikipedia].

MathML uses a special syntax to describe subscripts and superscripts for both, postscripts and prescripts, attached to a base expression:
<syntaxhighlight>
<mmultiscripts>
    base
     (subscript superscript)*
     [ <mprescripts/> (presubscript presuperscript)* ]
</mmultiscripts>
</syntaxhighlight>
After the base expression you can specify a postsubscript and a postsuperscript. Prescripts are optional and are separated by the empty tag <mprescripts/>. In addition you are able to use <none/> as a placeholder for empty positions.


== Attributes ==
<dl>
  <dt id="attr-subscriptshift">
    subscriptshift</dt>
  <dd>
    The minimum space by which to shift the subscript below the baseline of the expression, as a CSS length.</dd>
  <dt id="attr-superscriptshift">
    superscriptshift</dt>
  <dd>
    The minimum space by which to shift the superscript above the baseline of the expression, as a CSS length.</dd>
</dl>