---
title: 'open'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[open](https://developer.mozilla.org/en-US/docs/Web/API/Window.open) Article]'
  - 'Microsoft Developer Network: [[open Method](http://msdn.microsoft.com/en-us/library/ie/ms536651(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Window
summary: 'Opens a new window and loads the document specified by a given URL.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/open

---
## Summary

Opens a new window and loads the document specified by a given URL.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var newwindow = window.open(/* see parameter list */);
```

## Parameters

### url

 Data-type
:   BSTR

**String** that specifies the URL of the document to display. If no URL is specified, a new window with **about:blank** is displayed.

### name

 Data-type
:   BSTR

**String** that specifies the name of the window. This name is used as the value for the [**TARGET**](/html/attributes/target) attribute on a **form** or an [**anchor**](/html/elements/a) element.

### features

 Data-type
:   BSTR

**String** that contains a list of items separated by commas. Each item consists of an option and a value, separated by an equals sign (for example, "fullscreen=yes, toolbar=yes"). The following values are supported.

### replace

 Data-type
:   any

**Boolean** that specifies whether the *url* creates a new entry or replaces the current entry in the window's history list. This parameter only takes effect if the *url* is loaded into the same window.

## Return Value

Returns an object of type DOM NodeDOM Node

**IHTMLWindow2**

Returns a reference to the new **window** object. Use this reference to access properties and methods on the new window.

**Internet Explorer 7 on Windows Vista:** Opening a new window from an application (other than the Internet Explorer process) may result in a null return value. This restriction occurs because Internet Explorer runs in protected mode, by default. One facet of protected mode prevents applications from having privileged access to Internet Explorer when that access spans process boundaries. Opening a new window by using this method generates a new process. For more information about protected mode, see Understanding and Working in Protected Mode Internet Explorer. This commonly occurs for applications that host the WebBrowser control.

## Examples

This example uses the **open** method to create a new window that contains Sample.htm. The new window is 200 pixels by 400 pixels and has a status bar, but it does not have a toolbar, menu bar, or address field.

``` js
window.open("Sample.htm",null,
    "height=200,width=400,status=yes,toolbar=no,menubar=no,location=no");
```

## Notes

### Remarks

By default, the **open** method creates a window that has a default width and height and the standard menu, toolbar, and other features of Internet Explorer. You can alter this set of features by using the *features* parameter. This parameter is a string consisting of one or more feature settings. When the *features* parameter is specified, the features that are not defined in the parameter are disabled. Therefore, when using the *features* parameter, it is necessary to enable all the features that are to be included in the new window. If the *features* parameter is not specified, the window features maintain their default values. In addition to enabling a feature by setting it to a specific value, simply listing the feature name also enables that feature for the new window. Most of the *features* specified in the window.open method are ignored if user has selected, "Always open pop-ups in a new tab" setting in the Internet options control panel. When a function fired by an event on any object calls the **open** method, the window.**open** method is implied.

    <script language="JScript">
    function myOpen() {
        open('about:blank');}
    </script>
    <body onclick="myOpen();">
    Click this page and window.open() is called.
    </body>

When an event on any object calls the **open** method, the document.**open** method is implied.

    <button onclick="open('Sample.htm');">
    Click this button and document.open() is called.
    </button>

Windows Internet Explorer 8. New windows and pop-ups always inherit the zoom level of the parent window. Internet Explorer 7. The **Back**, **Forward**, and **Stop** commands are now located in the Navigation bar of the user interface. Prior to Internet Explorer 7 navigation commands were located in the toolbar. Internet Explorer 7 on Windows Vista. Opening a new window from an application other than the Internet Explorer process may result in a NULL return value. This occurs because Internet Explorer runs in protected mode by default. Protected mode prevents applications from privileged access to Internet Explorer when that access spans process boundaries. Because this method opens windows in a new process, protected mode restricts access to the new window. For more information, please see Understanding and Working in Protected Mode Internet Explorer. Internet Explorer 6 for Windows XP SP2 places several restrictions on windows created with this method. For several of the parameter values listed in the Parameters table, these restrictions are indicated by the minimum value. For more information, see About Window Restrictions. This method must use a user-initiated action, such as clicking on a link or tabbing to a link and pressing enter, to open a pop-up window. The Pop-up Blocker feature in Internet Explorer 6 blocks windows that are opened without being initiated by the user. The Pop-up Blocker also prevents windows from appearing if you call this method from an [**onunload**](/dom/Element/unload) event. In Internet Explorer 6, the **\_media** value of the *name* parameter specifies that this method loads a URL into the HTML content area of the Media Bar. Internet Explorer 5 allows further control over windows through the implementation of `title` in the *features* parameter of the **open** method. Turn off the title bar by opening the window from a trusted application, such as Microsoft Visual Basic or an HTML Application (HTA). These applications are considered trusted, because each uses Internet Explorer interfaces instead of the browser. In Windows CE, the [Document](/dom/Document) object is not available through scripting for a **window** opened using the **open** method.
