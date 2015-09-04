---
title: cookieEnabled
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Retrieves whether client-side persistent cookies are enabled. Persistent cookies are those that are stored on the client-side computer.'
uri: dom/Navigator/cookieEnabled

---
# cookieEnabled

## Summary

Retrieves whether client-side persistent cookies are enabled. Persistent cookies are those that are stored on the client-side computer.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Navigator](/dom/Navigator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = navigator.cookieEnabled;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

false (false)

Client does not support cookies or cookies are disabled.

true (true)

Client does support cookies.

## Examples

``` {.js}
if (!navigator.cookieEnabled) {
  // let the user know that enabling cookies makes the web page much more useful
}
```

## Usage

     Some websites may require cookies to be enabled on the client in order to work as intended.

eg. a cookie may be used to store a user token that is used to automatically log a user back in when they return visit.

Use navigator.cookieEnabled to determine if the client web browser has cookies enabled. Display a message if they are not and your site requires it.

## Notes

### Remarks

**Note**  CookieEnabled does not check the status of session cookies. This property does not check whether third-party persistent cookies are enabled.

### Syntax

## See also

### External resources

[How to enable cookies in your Web Browser](http://www.wikihow.com/Enable-Cookies-in-Your-Internet-Web-Browser)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.cookieEnabled](https://developer.mozilla.org/en-US/docs/Web/API/Navigator.cookieEnabled) Article]

Portions of this content come from the Microsoft Developer Network: [[navigator.cookieEnabled](http://msdn.microsoft.com/en-us/library/ie/ms533694(v=vs.85).aspx) Article]

