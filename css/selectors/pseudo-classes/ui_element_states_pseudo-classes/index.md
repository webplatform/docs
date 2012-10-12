== The <code>:enabled</code> and <code>:disabled</code> pseudo-classes ==
The <code>:enabled</code> pseudo-class represents user interface elements that are in an enabled state; such elements have a corresponding disabled state.

Conversely, the <code>:disabled</code> pseudo-class represents user interface elements that are in a disabled state; such elements have a corresponding enabled state.

What constitutes an enabled state, a disabled state, and a user interface element is language-dependent. In a typical document most elements will be neither <code>:enabled</code> nor <code>:disabled</code>.

<blockquote>'''Note:''' CSS properties that might affect a user’s ability to interact with a given user interface element do not affect whether it matches <code>:enabled</code> or <code>:disabled</code>; e.g., the display and visibility properties have no effect on the enabled/disabled state of an element. </blockquote>

== The :checked pseudo-class ==
Radio and checkbox elements can be toggled by the user. Some menu items are "checked" when the user selects them. When such elements are toggled "on" the <code>:checked</code> pseudo-class applies. While the <code>:checked</code> pseudo-class is dynamic in nature, and can altered by user action, since it can also be based on the presence of semantic attributes in the document, it applies to all media. For example, the <code>:checked</code> pseudo-class initially applies to such elements that have the HTML4 selected and checked attributes as described in [http://www.w3.org/TR/REC-html40/interact/forms.html#h-17.2.1 Section 17.2.1 of HTML4], but of course the user can toggle "off" such elements in which case the <code>:checked</code> pseudo-class would no longer apply.

== The :indeterminate pseudo-class ==
<blockquote>'''Note:''' Radio and checkbox elements can be toggled by the user, but are sometimes in an indeterminate state, neither checked nor unchecked. This can be due to an element attribute, or DOM manipulation.

A future version of this specification may introduce an :indeterminate pseudo-class that applies to such elements. </blockquote>

[[Category:CSS]]