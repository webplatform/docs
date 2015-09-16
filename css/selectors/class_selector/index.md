---
title: 'class selector'
tags:
  - CSS
uri: 'css/selectors/class selector'

---
Working with HTML, authors may use the "period" notation (also known as "full stop", U+002E, .) as an alternative to the \~= notation when representing the class attribute. Thus, for HTML, div.value and `div[class~=value]` have the same meaning. The attribute value must immediately follow the full stop (`.`).

UAs may apply selectors using the period (`.`) notation in XML documents if the UA has namespace-specific knowledge that allows it to determine which attribute is the "class" attribute for the respective namespace. One such example of namespace-specific knowledge is the prose in the specification for a particular namespace (e.g. SVG 1.0 [SVG11](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#SVG11) describes the SVG class attribute and how a UA should interpret it, and similarly MathML 1.01 [MATHML](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#MATHML) describes the MathML class attribute.)

## CSS examples:

We can assign style information to all elements with `class~="pastoral"` as follows:

``` css
*.pastoral { color: green }  /* all elements with class~=pastoral */
```

 or just

``` css
.pastoral { color: green }  /* all elements with class~=pastoral */
```

 The following assigns style only to H1 elements with `class~="pastoral"`:

``` css
H1.pastoral { color: green }  /* H1 elements with class~=pastoral */
```

 Given these rules, the first H1 instance below would not have green text, while the second would:

``` html
<H1>Not green</H1>
<H1 class="pastoral">Very green</H1>
```

 The following rule matches any P element whose class attribute has been assigned a list of whitespace-separated values that includes both pastoral and marine:

``` css
p.pastoral.marine { color: green }
```

 This rule matches when `class="pastoral blue aqua marine"` but does not match for `class="pastoral blue"`.

> **Note:** Because CSS gives considerable power to the "class" attribute, authors could conceivably design their own "document language" based on elements with almost no associated presentation (such as DIV and SPAN in HTML) and assigning style information through the "class" attribute. Authors should avoid this practice since the structural elements of a document language often have recognized and accepted meanings and author-defined classes may not.

> **Note:** If an element has multiple class attributes, their values must be concatenated with spaces between the values before searching for the class. As of this time the working group is not aware of any manner in which this situation can be reached, however, so this behavior is explicitly non-normative in this specification.
