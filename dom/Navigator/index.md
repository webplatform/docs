---
title: 'Navigator'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Navigator Object](https://developer.mozilla.org/en-US/docs/Web/API/Navigator) Article]'
  - 'Microsoft Developer Network: [[Navigator Object](http://msdn.microsoft.com/en-us/library/ie/ms535867(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [[Feature Detection](https://www.google.com/url?q=http://www.html5rocks.com/en/tutorials/detection/&sa=U&ei=U4y6U56ADIe7oQTPwYHgDw&ved=0CAUQFjAA&client=internal-uds-cse&usg=AFQjCNFIYgE2cg8o8GGC9hcD-nOloJxkEw) article]'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
notes:
  - "New listing page with proper object capitalization; replaces navigator.\nmissing properties for\ngetGamepads, dom/Navigator/getGamepads\ngetUserMedia, dom/Navigator/getUserMedia\n\njavaEnabled, dom/Navigator/javaEnabled"
readiness: 'In Progress'
summary: 'The navigator object contains state and identity information about the browser/user agent.'
tags:
  - API_Objects
  - DOM
uri: dom/Navigator

---
## Summary

The navigator object contains state and identity information about the browser/user agent.

## Properties

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

## Methods

[getGamepads](/dom/Navigator/getGamepads)
:   Retrieves a snapshot of the data for the currently connected and interacted-with gamepads. Returns a [Gamepad](/apis/gamepad/Gamepad) object.

[getUserMedia](/dom/Navigator/getUserMedia)
:   Prompts the user for permission to use a media device such as a camera or microphone. If the user provides permission, the `successCallback` is invoked on the calling application with a [LocalMediaStream](/apis/webrtc/LocalMediaStream) object as its argument.

[javaEnabled](/dom/Navigator/javaEnabled)
:   This method indicates whether the current browser is Java Run Time Environment-enabled or not.

[sendBeacon](/dom/Navigator/sendBeacon)
:   Asynchronously queues small amounts of HTTP data for transfer from the user agent to a web server. For example, it can be used to send analytics or diagnostics code without delaying the page's unload or affecting the performance of the navigation.

## Events

*No events.*

## Examples

[object Navigator] example enumerates the window.navigator object and displays the results in the web page.

``` js

```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Commonly used for feature detection of a web browser capabilities. java RTE and cookie support.

Avoid UserAgent sniffing of the navigator.userAgent property as this is not a reliable indicator of the userAgent's actual version number.

