---
title: mmultiscripts
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mmultiscripts)'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mmultiscripts element allows you to create tensor-like objects.'
tags:
  - Markup
  - Elements
  - MathML
uri: mathml/elements/mmultiscripts

---
## <span>Summary</span>

The MathML mmultiscripts element allows you to create tensor-like objects.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## <span>Examples</span>

These examples demonstrate a simple usage of the mmultiscripts element:

``` html


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
```

</pre>

## <span>Related specifications</span>

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mmultiscripts)
:   W3C Recommendation

In a descriptive way [tensors](http://en.wikipedia.org/wiki/Tensor) are multidimensional matrices (mathematical imprecise but exemplified). The degree of a tensor depends on the dimensionality of a representative array. For example, a number is a 0-dimensional array, or a 0th-order tensor. A 1-dimensional array (e.g. vectors) is a 1st-order tensor and so 2nd-order tensors are needed to represent square matrices. To learn more about the mathematical background of tensors refer to the [entry on Wikipedia](http://en.wikipedia.org/wiki/Tensor).

MathML uses a special syntax to describe subscripts and superscripts for both, postscripts and prescripts, attached to a base expression:

``` html
<mmultiscripts>
    base
     (subscript superscript)*
     [ <mprescripts/> (presubscript presuperscript)* ]
</mmultiscripts>
```

After the base expression you can specify a postsubscript and a postsuperscript. Prescripts are optional and are separated by the empty tag \<mprescripts/\>. In addition you are able to use \<none/\> as a placeholder for empty positions.

## <span>Attributes</span>

 subscriptshift
:   The minimum space by which to shift the subscript below the baseline of the expression, as a CSS length.
 superscriptshift
:   The minimum space by which to shift the superscript above the baseline of the expression, as a CSS length.
