The negation pseudo-class, <code>:not(X)</code>, is a functional notation taking a [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#simple-selectors-dfn|simple selector] (excluding the negation pseudo-class itself) as an argument. It represents an element that is not represented by its argument.

Negations may not be nested; <code>:not(:not(...))</code> is invalid. Note also that since pseudo-elements are not simple selectors, they are not a valid argument to <code>:not()</code>.

==Examples:==
The following selector matches all button elements in an HTML document that are not disabled.
<syntaxhighlight lang="css">
button:not([DISABLED])
</syntaxhighlight>
The following selector represents all but FOO elements.
<syntaxhighlight lang="css">
*:not(FOO)
</syntaxhighlight>
The following group of selectors represents all HTML elements except links.
<syntaxhighlight lang="css">
html|*:not(:link):not(:visited)
</syntaxhighlight>

Default namespace declarations do not affect the argument of the negation pseudo-class unless the argument is a universal selector or a type selector. 

Assuming that the default namespace is bound to "http://example.com/", the following selector represents all elements that are not in that namespace:
<syntaxhighlight lang="css">
*|*:not(*)
</syntaxhighlight>
The following selector matches any element that is not being hovered, regardless of its namespace. In particular, it is not limited to only matching elements in the default namespace that are not being hovered, and elements not in the default namespace don't match the rule when they are being hovered.
<syntaxhighlight lang="css">
*|*:not(:hover)
</syntaxhighlight>

<blockquote>'''Note:''' the <code>:not()</code> pseudo allows useless selectors to be written. For instance <code>:not(*|*)</code>, which represents no element at all, or <code>foo:not(bar)</code>, which is equivalent to foo but with a higher specificity. </blockquote>