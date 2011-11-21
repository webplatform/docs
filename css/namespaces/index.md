CSS Namespaces module defines syntax for using namespaces in CSS. It defines the <code>@namespace</code> rule for declaring a default namespace and for binding namespaces to namespace prefixes. It also defines a syntax for using those prefixes to represent namespace-qualified names. It does not define where such names are valid or what they mean: that depends on their context and is defined by a host language, such as Selectors, that references the syntax defined in the CSS Namespaces module.


== @namespace ==
The @namespace at-rule declares a namespace prefix and associates it with a given namespace name (a string). This namespace prefix can then be used in namespace-qualified names such as the CSS qualified names defined below.

=== Example A ===
This rule declares a default namespace http://www.w3.org/1999/xhtml to be applied to names that have no explicit namespace component.
<pre>
@namespace "http://www.w3.org/1999/xhtml";
</pre>

=== Example B ===
This rule declares a namespace prefix svg that is used to apply the namespace http://www.w3.org/2000/svg where the svg namespace prefix is used.
<pre>
@namespace svg "http://www.w3.org/2000/svg";
</pre>


== See also ==
*[http://www.w3.org/TR/css3-namespace/CSS Namespaces Module Specification]
*[[CSS/Training|CSS Educational Materials for Beginners]]
*[[CSS/Properties|CSS Properties Reference]]
*[[CSS/Selectors|CSS Selectors Reference]]

[[Category:CSS]]