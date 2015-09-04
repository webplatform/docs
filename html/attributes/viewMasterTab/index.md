---
title: viewMasterTab
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Deletion Candidate'
uri: html/attributes/viewMasterTab
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/focus
    - dom/events/activate
    - dom/defaultSelected
    - dom/properties/viewLink

---
# viewMasterTab

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Tabbing order goes from every tab stop within the viewlink to every tab stop in the primary document, based on sequence and [**tabIndex**](/html/attributes/tabIndex) value. By default, the master element participates in the tab sequence of the primary document, even if there are no tab stops defined within the viewlink. When using a viewlink, the **body** element inside the viewlink is not tabbable by default; the author must set the [**tabIndex**](/html/attributes/tabIndex) property if the behavior is designed to display a focus rectangle on the linked document. Setting the **tabIndex** property on the **body** of the document fragment causes the [**onfocus**](/w/index.php?title=dom/events/focus&action=edit&redlink=1) and [**onactivate**](/w/index.php?title=dom/events/activate&action=edit&redlink=1) events to fire when the viewlink document **body** receives focus.

### Syntax

## See also

### Related pages (MSDN)

-   `defaults`
-   `Reference`
-   `viewLink`
-   `Conceptual`
-   `Introduction to Viewlink`
-   `About Element Behaviors`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

