Selectors allow the representation of an element's attributes. When a selector is used as an expression to match against an element, attribute selectors must be considered to match an element if that element has an attribute that matches the attribute represented by the attribute selector.

The following attribute selectors exist:
* Presence and value selectors:
** <code>[[css/selectors/attributes/existence|[attributename]]]</code>
** <code>[[css/selectors/attributes/equality|[attributename="val"]]]</code>
** <code>[[css/selectors/attributes/whitespace|[attributename~="val"]]]</code>
** <code>[[css/selectors/attributes/hyphen|[attributename{{!}}="val"]]]</code>
* Substring matching selectors:
** <code>[[css/selectors/attributes/prefix|[attributename^="val"]]]</code>
** <code>[[css/selectors/attributes/suffix|[attributename$="val"]]]</code>
** <code>[[css/selectors/attributes/substring|[attributename*="val"]]]</code>

== Examples ==
The following attribute selector represents an h1 element that carries the title attribute, whatever its value:
<syntaxhighlight lang="css">h1[title]</syntaxhighlight>

In the following example, the selector represents a span element whose class attribute has exactly the value "example":
<syntaxhighlight lang="css">span[class="example"]</syntaxhighlight>

Multiple attribute selectors can be used to represent several attributes of an element, or several conditions on the same attribute. Here, the selector represents a span element whose hello attribute has exactly the value "Cleveland" and whose goodbye attribute has exactly the value "Columbus":

<syntaxhighlight lang="css">span[hello="Cleveland"][goodbye="Columbus"]</syntaxhighlight>

The following CSS rules illustrate the differences between "=" and "~=". The first selector would match, for example, an a element with the value "copyright copyleft copyeditor" on a rel attribute. The second selector would only match an a element with an href attribute having the exact value "http://www.w3.org/".

<syntaxhighlight lang="css">a[rel~="copyright"] { ... }
a[href="http://www.w3.org/"] { ... }</syntaxhighlight>

The following selector represents an a element whose hreflang attribute is exactly "fr".

<syntaxhighlight lang="css">a[hreflang=fr]</syntaxhighlight>

The following selector represents an a element for which the value of the hreflang attribute begins with "en", including "en", "en-US", and "en-scouse":

<syntaxhighlight lang="css">a[hreflang|="en"]</syntaxhighlight>

The following selectors represent a DIALOGUE element whenever it has one of two different values for an attribute character:

<syntaxhighlight lang="css">DIALOGUE[character=romeo]
DIALOGUE[character=juliet]</syntaxhighlight>

The following selector represents an HTML object, referencing an image:

<syntaxhighlight lang="css">object[type^="image/"]</syntaxhighlight>

The following selector represents an HTML anchor a with an href attribute whose value ends with ".html".

<syntaxhighlight lang="css">a[href$=".html"]</syntaxhighlight>

The following selector represents an HTML paragraph with a title attribute whose value contains the substring "hello"

<syntaxhighlight lang="css">p[title*="hello"]</syntaxhighlight>

[[Category:CSS]]