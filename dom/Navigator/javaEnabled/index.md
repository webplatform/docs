---
title: javaEnabled
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'This method indicates whether the current browser is Java Run Time Environment-enabled or not.'
uri: dom/Navigator/javaEnabled

---
# javaEnabled

## Summary

This method indicates whether the current browser is Java Run Time Environment-enabled or not.

*Method of [dom/Navigator](/dom/Navigator)*

## Syntax

``` {.js}
var result = navigator.javaEnabled();
```

## Return Value

Returns an object of type Boolean.

Boolean

**Boolean**. Returns one of the following possible values:

Return value
:   Description
true
:   Java JRE is enabled.
false
:   Java JRE is not enabled.

Â

## Examples

Feature test for Java JRE. Negative results do not mean that Java JRE is not installed on the client. It can also indicate that the Java JRE has been disabled by the client Addons Manager or the Java JRE control panel.

``` {.js}
if (window.navigator.javaEnabled()) {
   // browser has java JRE and it is enabled.
}
```

## Usage

     Feature testing for Java JRE support.

This usage scenario can be unreliable as the client may have disabled JRE.

Alternatively use text fallbacks for your applet and object tags that are using Java JRE. eg.

\<applet\> your browser does not have Java JRE installed or it has been disabled. \</applet\>

\<object\> your browser does not have Java JRE installed or it has been disabled. \</object\>

Note that the \<applet\> tag has been depreciated in html5. Use the \<object\> tag instead.

## Notes

This method does NOT determine if javascript or active scripting is enabled in the web browser or not. To detect if active scripting is enabled in a web browser add \<noscript\> tags to your web page.

The return value for this method indicates whether the preference that controls Java Run Time Environment is on or off - not whether the browser offers Java support in general.

Java JRE can also be disabled from the web browser's Addons manager or the Java JRE control panel.

## See also

### Other articles

[Download Java JRE from java.com](http://java.com)

[JavaTester.org - All about Java JRE](http://javatester.org)

[Test the version of Java JRE your browser is using](http://javatester.org/version.html)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[javaEnabled Method](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins.javaEnabled) Article]

Portions of this content come from the Microsoft Developer Network: [[javaEnabled Method](http://msdn.microsoft.com/en-us/library/ie/ms536610(v=vs.85).aspx) Article]

