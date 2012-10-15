Dynamic pseudo-classes classify elements on characteristics other than their name, attributes, or content, in principle characteristics that cannot be deduced from the document tree.

Dynamic pseudo-classes do not appear in the document source or document tree. The following pseudo-classes exist:

* [[css/selectors/pseudo-classes/:link|:link]]
* [[css/selectors/pseudo-classes/:visited|:visited]]
* [[css/selectors/pseudo-classes/:hover|:hover]]
* [[css/selectors/pseudo-classes/:active|:active]]
* [[css/selectors/pseudo-classes/:focus|:focus]]

=Examples=
<syntaxhighlight lang="css">
a:link    /* unvisited links */
a:visited /* visited links */
a:hover   /* user hovers */
a:active  /* active links */
</syntaxhighlight>

An example of combining dynamic pseudo-classes:
<syntaxhighlight lang="css">
a:focus
a:focus:hover
</syntaxhighlight>

The last selector matches <code>a</code> elements that are in the pseudo-class <code>:focus</code> and in the pseudo-class <code>:hover</code>.

<blockquote>'''Note:''' An element can be both ‘<code>:visited</code>’ and ‘<code>:active</code>’ (or ‘<code>:link</code>’ and ‘<code>:active</code>’).</blockquote>

[[Category:CSS]]