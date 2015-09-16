---
title: 'keygen'
compatibility:
  feature: keygen
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLKeygenElement](/w/index.php?title=dom/HTMLKeygenElement&action=edit&redlink=1)'
standardization_status: 'W3C Recommendation'
summary: 'Represents a key pair generator control'
tags:
  - Markup
  - Elements
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLKeygenElement
uri: html/elements/keygen

---
## Summary

Represents a key pair generator control

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLKeygenElement](/w/index.php?title=dom/HTMLKeygenElement&action=edit&redlink=1)

When the control's form is submitted, the private key is stored in the local keystore, and the public key is packaged and sent to the server.

## HTML Attributes

-   `autofocus` = boolean
    Allows the author to indicate that a control is to be focused as soon as the page is loaded
-   `challenge` = string
    A challenge string that is submitted along with the public key. [[Example A]](#Example_A)
-   `disabled` = boolean
    If present, make the control non-interactive and to prevent its value from being submitted.
-   `form` = the ID of a form element in the element's owner
    Associate the keygen element with its form owner.
    By default, the keygen element is associated with its nearest ancestor form element.
-   `keytype` = rsa
    The type of key generated.
-   `name` = unique name
    Represents the element's name.

## Examples

``` html

<keygen name="key" challenge="235ldahlae983dadfar"/>

```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-keygen-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-keygen-element)
:   W3C Recommendation

