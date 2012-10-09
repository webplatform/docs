Selectors allow the representation of an element's attributes. When a selector is used as an expression to match against an element, attribute selectors must be considered to match an element if that element has an attribute that matches the attribute represented by the attribute selector.

== Attribute presence and value selectors ==
CSS2 introduced four attribute selectors:

* <code>[att]</code> Represents an element with the att attribute, whatever the value of the attribute.  
* <code>[att=val]</code> Represents an element with the att attribute whose value is exactly "val". 
* <code>[att~=val]</code> Represents an element with the att attribute whose value is a whitespace-separated list of words, one of which is exactly "val". If "val" contains whitespace, it will never represent anything (since the words are separated by spaces). Also if "val" is the empty string, it will never represent anything.  
* <code>[att|=val]</code> Represents an element with the att attribute, its value either being exactly "val" or beginning with "val" immediately followed by "-" (U+002D). This is primarily intended to allow language subcode matches (e.g., the hreflang attribute on the a element in HTML) as described in BCP 47 ([BCP47]) or its successor. For lang (or xml:lang) language subcode matching, please see the :lang pseudo-class. 

Attribute values must be CSS identifiers or strings. [CSS21] The case-sensitivity of attribute names and values in selectors depends on the document language.

<code><pre>
Examples:

The following attribute selector represents an h1 element that carries the title attribute, whatever its value:

h1[title]

In the following example, the selector represents a span element whose class attribute has exactly the value "example":

span[class="example"]

Multiple attribute selectors can be used to represent several attributes of an element, or several conditions on the same attribute. Here, the selector represents a span element whose hello attribute has exactly the value "Cleveland" and whose goodbye attribute has exactly the value "Columbus":

span[hello="Cleveland"][goodbye="Columbus"]

The following CSS rules illustrate the differences between "=" and "~=". The first selector would match, for example, an a element with the value "copyright copyleft copyeditor" on a rel attribute. The second selector would only match an a element with an href attribute having the exact value "http://www.w3.org/".

a[rel~="copyright"] { ... }
a[href="http://www.w3.org/"] { ... }

The following selector represents an a element whose hreflang attribute is exactly "fr".

a[hreflang=fr]

The following selector represents an a element for which the value of the hreflang attribute begins with "en", including "en", "en-US", and "en-scouse":

a[hreflang|="en"]

The following selectors represent a DIALOGUE element whenever it has one of two different values for an attribute character:

DIALOGUE[character=romeo]
DIALOGUE[character=juliet]
</pre></code>

== Substring matching attribute selectors ==
Three additional attribute selectors are provided for matching substrings in the value of an attribute:

* <code>[att^=val]</code> Represents an element with the att attribute whose value begins with the prefix "val". If "val" is the empty string then the selector does not represent anything.  
* <code>[att$=val]</code> Represents an element with the att attribute whose value ends with the suffix "val". If "val" is the empty string then the selector does not represent anything.  
* <code>[att*=val]</code> Represents an element with the att attribute whose value contains at least one instance of the substring "val". If "val" is the empty string then the selector does not represent anything.

Attribute values must be CSS identifiers or strings. [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS21 CSS21] The case-sensitivity of attribute names in selectors depends on the document language.

<code><pre>
Examples:

The following selector represents an HTML object, referencing an image:

object[type^="image/"]

The following selector represents an HTML anchor a with an href attribute whose value ends with ".html".

a[href$=".html"]

The following selector represents an HTML paragraph with a title attribute whose value contains the substring "hello"

p[title*="hello"]
</pre></code>
[[Category:CSS]]