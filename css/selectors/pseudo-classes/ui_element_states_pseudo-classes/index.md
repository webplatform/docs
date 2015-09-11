---
title: ui element states pseudo-classes
tags:
  - CSS
uri: 'css/selectors/pseudo-classes/ui element states pseudo-classes'

---
## <span>The `:enabled` and `:disabled` pseudo-classes</span>

The `:enabled` pseudo-class represents user interface elements that are in an enabled state; such elements have a corresponding disabled state.

Conversely, the `:disabled` pseudo-class represents user interface elements that are in a disabled state; such elements have a corresponding enabled state.

What constitutes an enabled state, a disabled state, and a user interface element is language-dependent. In a typical document most elements will be neither `:enabled` nor `:disabled`.

> **Note:** CSS properties that might affect a user’s ability to interact with a given user interface element do not affect whether it matches `:enabled` or `:disabled`; e.g., the display and visibility properties have no effect on the enabled/disabled state of an element.

## <span>The :checked pseudo-class</span>

Radio and checkbox elements can be toggled by the user. Some menu items are "checked" when the user selects them. When such elements are toggled "on" the `:checked` pseudo-class applies. While the `:checked` pseudo-class is dynamic in nature, and can altered by user action, since it can also be based on the presence of semantic attributes in the document, it applies to all media. For example, the `:checked` pseudo-class initially applies to such elements that have the HTML4 selected and checked attributes as described in [Section 17.2.1 of HTML4](http://www.w3.org/TR/REC-html40/interact/forms.html#h-17.2.1), but of course the user can toggle "off" such elements in which case the `:checked` pseudo-class would no longer apply.

## <span>The :indeterminate pseudo-class</span>

> **Note:** Radio and checkbox elements can be toggled by the user, but are sometimes in an indeterminate state, neither checked nor unchecked. This can be due to an element attribute, or DOM manipulation. A future version of this specification may introduce an :indeterminate pseudo-class that applies to such elements.