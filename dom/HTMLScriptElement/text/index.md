---
title: text
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Final review.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLScriptElement
    href: /dom/HTMLScriptElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLScriptElement
standardization_status: 'W3C Last Call Working Draft'
summary: 'Legacy. Use textContent instead. When setting, does same as textContent. When getting, gets a concatenated version of all of the child text nodes of a script element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLScriptElement/text

---
## <span>Summary</span>

Legacy. Use textContent instead. When setting, does same as textContent. When getting, gets a concatenated version of all of the child text nodes of a script element.

Property of [dom/HTMLScriptElement](/dom/HTMLScriptElement)[dom/HTMLScriptElement](/dom/HTMLScriptElement)

## <span>Syntax</span>

``` js
var scriptCode = scriptElement.text;
scriptElement.text = newScriptCode;
```

## <span>Return Value</span>

Returns an object of type StringString

A concatenation of all of the child [text nodes](/dom/Text) of the element.

## <span>Examples</span>

The following script gets the code of an inline script element, changes the name of a function, constructs a new scripts element, sets the changed code as its code and appends it to the document in order to run it.

``` js
// Caching the script element with the some-script ID.
var script = document.getElementById("some-script");

// Getting the script code.
// Alternatively, use script.textContent.
var scriptCode = script.text;

// Replacing the first occurrence of "function someFunction()"
// with "function newFunction()".
scriptCode = scriptCode.replace("function someFunction()", "function newFunction()");

// Creating a new script element.
var newScript = document.createElement("script");

// Setting the changed script code as its text.
// Alternatively, use newScript.textContent.
newScript.text = scriptCode;

// Appending the script element to the head element
// in order to run it.
document.head.appendChild(newScript);
```

## <span>Usage</span>

     Legacy. Use textContent instead.

Use this property to get a concatenated version of all of the child text nodes of a [script](/html/elements/script) element. Setting this property works the same way as setting the [textContent](/dom/Node/textContent) property.

## <span>Notes</span>

-   [Text nodes](/dom/Text) that are nested within elements or HTML comments are excluded.
-   Settings this property of a [**script**](/html/elements/script) element after its contained or referenced script has already ran does not run the new set code.

## <span>Related specifications</span>

[Document Object Model (DOM) Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-46872999)
:   W3C Recommendation

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/scripting.html#dom-script-text)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/scripting-1.html#dom-script-text)
:   W3C Last Call Working Draft
