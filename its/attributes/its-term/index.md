---
title: 'its-term'
code_samples:
  - 'http://gist.github.com/8404173'
compatibility:
  feature: its-term
  topic: its
notes:
  - 'Add summery, example, note, compatibility.'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The its-term attribute is used to mark terms so they can be recognized during translation process. This helps to increase consistency of translation across different parts of the documentation.'
tags:
  - Markup_Attributes
  - Internationalization
uri: its/attributes/its-term

---
## Summary

The its-term attribute is used to mark terms so they can be recognized during translation process. This helps to increase consistency of translation across different parts of the documentation.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[/dom/HTMLElement](/dom/HTMLElement)

</td>
</tr>
</table>
The its-term attribute can contain "yes" or "no" values. Defintion of the term can be optionally linked by using its-term-info-ref attribute.

## Examples

``` html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Terminology test: default</title>
  </head>
  <body>
    <p>We need a new <span its-term="yes">motherboard</span></p>
  </body>
</html>
```

</pre>
[View live example](http://gist.github.com/8404173)

## Usage

     Use its-term for all terms on your page especially if you expect your content being translated to other languages in the future.

## Related specifications

[Internationalization Tag Set (ITS) Version 2.0](http://www.w3.org/TR/its20/)
:   W3C Recommendation
