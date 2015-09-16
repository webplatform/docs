---
title: 'id selector'
tags:
  - CSS
uri: 'css/selectors/id selector'

---
Document languages may contain attributes that are declared to be of type ID. What makes attributes of type ID special is that no two such attributes can have the same value in a conformant document, regardless of the type of the elements that carry them; whatever the document language, an ID typed attribute can be used to uniquely identify its element. In HTML all ID attributes are named "id"; XML applications may name ID attributes differently, but the same restriction applies.

An ID-typed attribute of a document language allows authors to assign an identifier to one element instance in the document tree. An ID selector contains a "number sign" (U+0023, \#) immediately followed by the ID value, which must be an CSS [identifiers](http://www.w3.org/TR/CSS21/syndata.html#value-def-identifier). An ID selector represents an element instance that has an identifier that matches the identifier in the ID selector.

Selectors does not specify how a UA knows the ID-typed attribute of an element. The UA may, e.g., read a document's DTD, have the information hard-coded or ask the user.

## Examples:

The following ID selector represents an h1 element whose ID-typed attribute has the value "chapter1":

``` css
h1#chapter1
```

 The following ID selector represents any element whose ID-typed attribute has the value "chapter1":

``` css
#chapter1
```

 The following selector represents any element whose ID-typed attribute has the value "z98y".

``` css
*#z98y
```

> **Note:** In XML 1.0 [XML10](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#XML10), the information about which attribute contains an element's IDs is contained in a DTD or a schema. When parsing XML, UAs do not always read the DTD, and thus may not know what the ID of an element is (though a UA may have namespace-specific knowledge that allows it to determine which attribute is the ID attribute for that namespace). If a style sheet author knows or suspects that a UA may not know what the ID of an element is, he should use normal attribute selectors instead: `[name=p371]` instead of \#p371.

If an element has multiple ID attributes, all of them must be treated as IDs for that element for the purposes of the ID selector. Such a situation could be reached using mixtures of xml:id, DOM3 Core, XML DTDs, and namespace-specific knowledge.
