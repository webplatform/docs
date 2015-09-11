---
title: cssom
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/vendor prefix'
uri: css/concepts/cssom

---
The CSSOM API offers a programmatic interface to various CSS features. A CSSOM *property name* corresponds to property names that appear in style sheets, but uses an alternate camelCase syntax. For example, the [**font-size**](/css/properties/font-size) property is represented in CSSOM as **fontSize**, and scripts can directly assign a value to **element.style.fontSize**. (Experimental or otherwise not fully standardized properties would be represented in style sheets using [vendor prefixes](/w/index.php?title=concepts/vendor_prefix&action=edit&redlink=1) such as **-webkit-font-size** and **-moz-font-size**, in which case corresponding CSSOM prefixes would be **WebkitFontSize** and **MozFontSize**.) Refer to <http://www.w3.org/TR/cssom/> for a list of the names.