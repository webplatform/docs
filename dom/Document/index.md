---
title: Document
notes:
  - 'New listing page with proper object capitalization; replaces document.'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Document is one of the most important objects in the DOM. It is where many API methods and properties are rooted.'
tags:
  - API
  - Objects
  - DOM
uri: dom/Document

---
## <span>Summary</span>

Document is one of the most important objects in the DOM. It is where many API methods and properties are rooted.

## <span>Properties</span>

API Name
:   Summary

[activeElement](/dom/Document/activeElement)
:   Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the `<body>` element.

[body](/dom/Document/body)
:   Gets or sets the [body](/html/elements/body) element of the document.

[characterSet](/dom/Document/characterSet)
:   Gets the preferred MIME name of the document's character encoding.

[charset](/dom/Document/charset)
:   Gets or sets the preferred MIME name of the document's character encoding.

[cookie](/dom/Document/cookie)
:   Sets or gets the string value of a cookie.

[defaultCharset](/dom/Document/defaultCharset)
:   Gets the default character set from the current regional language settings.

[defaultView](/dom/Document/defaultView)
:   Returns the Document's browsing context's Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.

[designMode](/dom/Document/designMode)
:   Sets or gets a value that indicates whether the document can be edited.

[doctype](/dom/Document/doctype)
:   Gets an object that represents the [document type declaration](/html/elements/!DOCTYPE) that is associated with the current **document**.

[documentElement](/dom/Document/documentElement)
:   Gets the root node of the document.

[domain](/dom/Document/domain)
:   Insecure. Use the web messaging API ([postMessage](/dom/Window/postMessage) and the [message](/dom/Window/message) event) instead. Gets or sets the security domain of the document.

[forms](/dom/Document/forms)
:   This property returns an object array representing an HTMLCollection of all the forms in the document.

[fullscreenElement](/dom/Document/fullscreenElement)
:   Exposes the current fullscreen state, returning the element that is displayed fullscreen, or `null` if there is no such element.

[fullscreenEnabled](/dom/Document/fullscreenEnabled)
:   Exposes the current document's fullscreen capability, returning `true` if the document can display elements in fullscreen, or `false` if not.

[head](/dom/Document/head)
:   Gets the [head](/html/elements/head) element of the document.

[hidden](/dom/Document/hidden)
:   document.hidden returns true if the document is hidden or false if it is visible at all

[images](/dom/Document/images)
:   Legacy method. Use [document.querySelectorAll("img")](/css/selectors_api/querySelectorAll) instead. Gets a live collection of [img](/html/elements/img) elements in a document.

[implementation](/dom/Document/implementation)
:

[inputEncoding](/dom/Document/inputEncoding)
:   Gets the character encoding that is used for the text that is loaded into the **document** object.

[lastModified](/dom/Document/lastModified)
:   Gets the date that the document was last modified, if the document supplies one.

[linkColor](/dom/Document/linkColor)
:

[links](/dom/Document/links)
:

[readyState](/dom/Document/readyState)
:   Retrieves a value that indicates the current state of the object.

[referrer](/dom/Document/referrer)
:   Gets the URL of the location that referred the user to the current document.

[scripts](/dom/Document/scripts)
:

[title](/dom/Document/title)
:   Gets or sets the title of a **Document**. When the document is the main document that is shown (meaning, not of an [iframe](/html/elements/iframe)), this is usually shown to the user.

[visibilityState](/dom/Document/visibilityState)
:   Returns the visibility state of a webpage.

[visibilitychange](/dom/Document/visibilitychange)
:   Set the visibility state of an element

[vlinkColor](/dom/Document/vlinkColor)
:

[xmlEncoding](/dom/Document/xmlEncoding)
:   Gets a value that represents the character encoding that is specified in the declaration of an XML document.

[xmlStandalone](/dom/Document/xmlStandalone)
:   Gets or sets the value of the **standalone** attribute in the declaration of an XML document.

[xmlVersion](/dom/Document/xmlVersion)
:   Gets or sets the **version** attribute that is specified in the declaration of an XML document.

## <span>Methods</span>

API Name
:   Summary

[adoptNode](/dom/Document/adoptNode)
:   Tries to move a node from one document to the document that the **document** object displays. It is preferable to use [importNode](/dom/Document/importNode) instead.

[close](/dom/Document/close)
:   Closes an output stream and forces the sent data to display.

[createAttribute](/dom/Document/createAttribute)
:   Creates an [**attribute**](/html/attributes) object with a specified [**name**](/html/attributes/name).

[createAttributeNS](/dom/Document/createAttributeNS)
:   Creates a reference to an [**attribute**](/html/attributes) object that is associated with an XML namespace.

[createCDATASection](/dom/Document/createCDATASection)
:   Creates a CDATA section that contains the specified text.

[createComment](/dom/Document/createComment)
:   Creates a **comment** object with the specified [**data**](/html/attributes/data).

[createDocumentFragment](/dom/Document/createDocumentFragment)
:   Creates a new document fragment (DocumentFragment) object.

[createElement](/dom/Document/createElement)
:   Creates an instance of the element for the specified tag.

[createElementNS](/dom/Document/createElementNS)
:   Creates an element from the specified namespace as a stand-alone object (unattached to the DOM).

[createEvent](/dom/Document/createEvent)
:   Creates a DOM event of the specified type. This method is deprecated; use event constructors ([CustomEvent](/dom/CustomEvent)) instead.

[createNodeIterator](/dom/Document/createNodeIterator)
:   Creates a [**NodeIterator**](/dom/NodeIterator) object that you can use to traverse filtered lists of nodes or elements in a document.

[createProcessingInstruction](/dom/Document/createProcessingInstruction)
:   Creates a [**processing instruction**](/dom/ProcessingInstruction) for an XML parser.

[createRange](/dom/Document/createRange)
:   Creates an empty [**Range**](/dom/Range) instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.

[createTextNode](/dom/Document/createTextNode)
:   Creates a text node containing the passed string (nodeValue).

[createTreeWalker](/dom/Document/createTreeWalker)
:   Creates a [**TreeWalker**](/dom/TreeWalker) object that you can use to traverse filtered lists of nodes or elements in a document.

[elementFromPoint](/dom/Document/elementFromPoint)
:   Returns the element at the specified x and y coordinates.

[exitFullscreen](/dom/Document/exitFullscreen)
:   The exitFullscreen method provides a way for exiting the fullscreen mode enabled by [requestFullscreen](/dom/Element/requestFullscreen).

[getElementById](/dom/Document/getElementById)
:   Gets an element with a specified ID.

[getElementsByClassName](/dom/Document/getElementsByClassName)
:   Gets a collection of all descendant elements with given classes. Not recommended; see Notes.

[getElementsByName](/dom/Document/getElementsByName)
:   Returns an HTMLCollection of elements in the document that have a `name` attribute with the specified value.

[getElementsByTagName](/dom/Document/getElementsByTagName)
:   Returns an HTMLCollection of all descendant elements with a given tag name.

[getElementsByTagNameNS](/dom/Document/getElementsByTagNameNS)
:   Returns an HTMLCollection of the elements with the specified tag name and namespace.

[getNamedFlows](/dom/Document/getNamedFlows)
:   Gathers [**NamedFlow**](/apis/css-regions/NamedFlow) objects, each representing a set of content that flows through various layout [regions](/css/concepts/region).

[hasFocus](/dom/Document/hasFocus)
:   Returns the focus state of the current document, `true` if the document has focus, `false` if not.

[importNode](/dom/Document/importNode)
:   Imports a node from another document into the the document that the **document** object displays.

[open](/dom/Document/open)
:

[register](/dom/Document/register)
:   Registers a new, custom element and returns the element's constructor.

[releaseCapture](/dom/Document/releaseCapture)
:   Removes mouse capture from the object in the current document.

[write](/dom/Document/write)
:   Method to insert a string of marked up text in the document tree.

[writeln](/dom/Document/writeln)
:

## <span>Events</span>

API Name
:   Summary

[rowenter](/dom/Document/rowenter)
:

[rowexit](/dom/Document/rowexit)
:

[rowsdelete](/dom/Document/rowsdelete)
:

[rowsinserted](/dom/Document/rowsinserted)
:

[scroll](/dom/Document/scroll)
:

[select](/dom/Document/select)
:

[selectionchange](/dom/Document/selectionchange)
:

[selectstart](/dom/Document/selectstart)
:

[start](/dom/Document/start)
:

[stop](/dom/Document/stop)
:

[storage](/dom/Document/storage)
:

[storagecommit](/dom/Document/storagecommit)
:

## <span>Examples</span>

``` js
if (document.title !== "") {
    console.log("The title is " + document.title)
}
```

This example shows an event handler function that displays the current position of the mouse, relative to the upper-left corner of the document, in a console window.

``` html
<!doctype html>
<html>
 <head>
  <title>Report mouse moves</title>
  <script>
    function reportMove()
    {
      console.log("X = " + window.event.x + ", Y = " + window.event.y);
    }
  </script>
 </head>
 <body onmousemove="reportMove()">
  <h1>Welcome!</h1>
 </body>
</html>
```

## <span>Usage</span>

     Use the document object to examine, modify, or add content to an HTML document and to process events within that document. In a script, the document object can be referenced through the document property of the window object or it can be referenced directly.

## <span>Related specifications</span>

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML)
:   Recommendation

[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)
:   Recommendation

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/dom.html)
:   Candidate Recommendation

