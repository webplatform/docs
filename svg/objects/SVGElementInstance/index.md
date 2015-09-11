---
title: SVGElementInstance
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
tags:
  - API
  - Objects
  - DOM
uri: svg/objects/SVGElementInstance

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Inherited from SVGElement</span>

### <span>Properties</span>

*No properties.*

### <span>Methods</span>

*No methods.*

### <span>Events</span>

*No events.*

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The root object in the instance tree is pointed to by the [**instanceRoot**](/svg/properties/instanceRoot) attribute on the [**SVGUseElement**](/svg/elements/use) object for the corresponding **use** element.

If the [**use**](/svg/elements/use) element references a simple graphics element such as [**rect**](/svg/elements/rect), there is only one **SVGElementInstance** object, and the [**correspondingElement**](/svg/properties/correspondingElement) attribute on this **SVGElementInstance** object is the **SVGRectElement** that corresponds to the referenced **rect** element.

If the [**use**](/svg/elements/use) element references a [**g**](/svg/elements/g) element that contains two [**rect**](/svg/elements/rect) elements, the instance tree contains three **SVGElementInstance** objects: a root **SVGElementInstance** object whose [**correspondingElement**](/svg/properties/correspondingElement) attribute is the **SVGGElement** object for the **g** element, and then two child **SVGElementInstance** objects that have their **correspondingElement** attribute that is an **SVGRectElement** object.

If the referenced object is a [**use**](/svg/elements/use) element, or if there are **use** subelements within the referenced object, the instance tree contains a recursive expansion of the indirect references to form a complete tree. For example, if a **use** element references a [**g**](/svg/elements/g) element, and the **g** element contains a **use** element, and that **use** element references a [**rect**](/svg/elements/rect) element, the instance tree for the original (outermost) **use** consists of a hierarchy of **SVGElementInstance** objects, as follows:

     SVGElementInstance #1 (parentNode=null, firstChild=#2, correspondingElement is the 'g')
       SVGElementInstance #2 (parentNode=#1, firstChild=#3, correspondingElement is the other 'use')
         SVGElementInstance #3 (parentNode=#2, firstChild=null, correspondingElement is the 'rect')

### <span>Standards information</span>

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.9

### <span>Members</span>

The **SVGElementInstance** object has these methods:

-   [**addEventListener**](/svg/methods/addListener): Registers an event listener
-   [**dispatchEvent**](/svg/methods/dispatchEvent): Dispatches an event to an object.
-   [**removeEventListener**](/svg/methods/removeListener): Removes an event listener.

The **SVGElementInstance** object has these properties:

-   [**childNodes**](/svg/properties/childNodes): Gets an [**SVGElementInstanceList**](/svg/objects/SVGElementInstanceList) object that contains all children of this **SVGElementInstance** object within the instance tree.
-   [**correspondingElement**](/svg/properties/correspondingElement): Gets the corresponding element that this object is an instance of.
-   [**correspondingUseElement**](/svg/properties/correspondingUseElement): Gets the corresponding [**use**](/svg/elements/use) element that this object belongs to.
-   [**firstChild**](/svg/properties/firstChild): Gets the first child of this **SVGElementInstance** object in the instance tree.
-   [**lastChild**](/svg/properties/lastChild): Gets the last child of this **SVGElementInstance** object in the instance tree.
-   [**nextSibling**](/svg/properties/nextSibling): Gets the **SVGElementInstance** object that immediately follows this **SVGElementInstance** object.
-   [**parentNode**](/svg/properties/parentNode): Gets the parent of this **SVGElementInstance** object within the instance tree.
-   [**previousSibling**](/svg/properties/previousSibling): Gets the **SVGElementInstance** object that immediately precedes this **SVGElementInstance** object.
