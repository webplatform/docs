---
title: 'translate'
compatibility:
  feature: translate
  topic: html
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The translate attribute indicates whether the element’s content and attribute values should be translated or not.'
tags:
  - Markup_Attributes
  - HTML
  - Internationalization
uri: html/attributes/translate

---
## Summary

The translate attribute indicates whether the element’s content and attribute values should be translated or not.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLElement](/dom/HTMLElement)

</td>
</tr>
</table>
Two values allowed: "yes" and "no". The information will be inherited. When no translate flag is set, "yes" is default.

Some automated translation services apply "no" to elements like the code element.

Elements with translate attributes of different values may be nested to indicate a chunk of text that should be translated within a container that should not be translated, or vice versa.

Overwriting "no" with "yes" is not widely supported by translation services yet.

## Examples

``` html


<p>The national motto of France is
<i lang="fr" translate="no">Liberté, Egalité, Fraternité</i>
(freedom, equality, brotherhood).</p>
```

</pre>

``` html


<code translate="no">
<section id="translate-attribute">
<h2><span translate="yes">The <span translate="no">translate</span> attribute<h2>
<p><span translate="yes">The <span translate="no">translate</span> attribute indicates whether the element’s content and attribute values should be translated or not.</span></p>
</section>
</code>
```

</pre>

## Related specifications

[HTML5](http://www.w3.org/TR/html5/)
:   W3C Recommendation

## See also

### External resources

[Using HTML's translate attribute](http://www.w3.org/International/questions/qa-translate-flag)
