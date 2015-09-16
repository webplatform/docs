---
title: 'close'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[window.close](https://developer.mozilla.org/en-US/docs/Web/API/Window.close) Article]'
  - 'Microsoft Developer Network: [[close Method](http://msdn.microsoft.com/en-us/library/ie/ms536367(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Closes the current browser window or tab, or HTML Application (HTA).'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/close

---
## Summary

Closes the current browser window or tab, or HTML Application (HTA).

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.close();
```

## Return Value

No return value

## Examples

``` js
<script type="text/javascript">
function closeCurrentWindow()
{
  window.close();
}
</script>
```

## Notes

### Remarks

When a function fired by an event on any object calls the **close** method, the window.**close** method is implied.

    <script type="text/javascript">
    function myClose() {
        close();}
    </script>
    <body onclick="myClose();">
    Click this page and window.close() is called.
    </body>

When an event on any object calls the **close** method, the [**Document.close**](/dom/Document/close) method is implied.

    <button type="button" onclick="close();">
    Click this button and document.close() is called.
    </button>

How a window is closed programmatically determines whether the user is prompted with a confirmation dialog box:

-   Invoking the window.**close** method on a window not opened with script displays a confirmation dialog box. Using script to close the last running instance of Windows Internet Explorer also opens the confirmation dialog box.
-   Invoking the

window.**close** method on an HTA closes the application without prompting the user because the HTA is trusted and follows a different security model. For more information on the security model of HTAs, please refer to [\_inet\_HTML\_Applications\_Overview\#Security\#Security The Power of Trust: HTAs and Security].

#### Using the close method in a Metro style app using JavaScript

Invoking the **window.close** method on a Metro style app using JavaScript closes the app without prompting the user. It is against Windows Store policy to programmatically close your app. The only time an app should programmatically close is when there is an unrecoverable error, in which case the app should throw an unhandled exception or use the **MSApp.terminateApp** method. In you use **window.close**, it appears as a crash to the user is logged as a crash in the developer’s telemetry data on the Windows Store dashboard.
