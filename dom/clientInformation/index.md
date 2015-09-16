---
title: 'clientInformation'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Navigator
    href: /dom/Navigator
tags:
  - API
  - Objects
  - DOM
uri: dom/clientInformation

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [Navigator](/dom/Navigator)[Navigator](/dom/Navigator)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from Navigator

### Properties

API Name
:   Summary

[appCodeName](/dom/Navigator/appCodeName)
:   Returns the internal "code" name of the current browser. Do not rely on this property to return the correct value.

[appMinorVersion](/dom/Navigator/appMinorVersion)
:   Retrieves the userAgent application's minor version value.

[appName](/dom/Navigator/appName)
:   appName Returns a string with the name of the browser/user agent.

    The HTML5 specification also allows any browser to return "Netscape" here, for compatibility reasons.

[appVersion](/dom/Navigator/appVersion)
:   Returns the version of the browser as a string. It may be either a plain version number, like "5.0", or a version number followed by more detailed information. The HTML5 specification also allows any browser to return "4.0" here, for compatibility reasons.

[constructor](/dom/Navigator/constructor)
:

[cookieEnabled](/dom/Navigator/cookieEnabled)
:   Retrieves whether client-side persistent cookies are enabled. Persistent cookies are those that are stored on the client-side computer.

[doNotTrack](/dom/Navigator/doNotTrack)
:   Returns the user's do-not-track setting. This is "yes" if the user has requested not to be tracked by web sites, content, or advertising.

[maxTouchPoints](/dom/Navigator/maxTouchPoints)
:   The maximum number of simultaneous touch contacts supported by the device.

[platform](/dom/Navigator/platform)
:   Retrieves the name of the user's operating system.

    In IE10 and higher and WaterFox browsers this will return the bitness of the current tab. eg

    Win32 or Win64.

[pointerEnabled](/dom/Navigator/pointerEnabled)
:   Indicates if the browser will fire pointer events for pointing input.

    In late 2013, pointerEnabled was removed from the specification as checking PointerEvent in Window object is sufficient for feature detection. Do not use this property and use PointerEvent instead.

[userLanguage](/dom/Navigator/userLanguage)
:   Retrieves the operating system's natural language setting.

    This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).

### Methods

API Name
:   Summary

[getGamepads](/dom/Navigator/getGamepads)
:   Retrieves a snapshot of the data for the currently connected and interacted-with gamepads. Returns a [Gamepad](/apis/gamepad/Gamepad) object.

[getUserMedia](/dom/Navigator/getUserMedia)
:   Prompts the user for permission to use a media device such as a camera or microphone. If the user provides permission, the `successCallback` is invoked on the calling application with a [LocalMediaStream](/apis/webrtc/LocalMediaStream) object as its argument.

[javaEnabled](/dom/Navigator/javaEnabled)
:   This method indicates whether the current browser is Java Run Time Environment-enabled or not.

[sendBeacon](/dom/Navigator/sendBeacon)
:   Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page's unload or affecting the performance of the navigation.

### Events

*No events.*

## Examples

This example shows how to determine whether the client can run Java applets.

``` js
if (window.clientInformation.javaEnabled()) {
    // Java is enabled; applets can run.
}
```

This example shows how to determine whether the **userAgent** of the browser contains "MSIE". If it does, the browser is Internet Explorer.

``` js
if (window.clientInformation.userAgent.indexOf( "MSIE " ) > 0) {
    // The browser is Microsoft Internet Explorer.
}
```

