---
title: 'doNotTrack'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[navigator.doNotTrack](https://developer.mozilla.org/en-US/docs/Web/API/navigator.doNotTrack) Article]'
  - 'Microsoft Developer Network: [[navigator.msDoNotTrack](http://msdn.microsoft.com/en-us/library/ie/gg699483(v=vs.85).aspx) Article]'
notes:
  - "MSDN documentation needs updating\nref to the latest draft.\nnavigator.msdoNotTracked dropped in favor of request headers.\n\nA screen shot of the Blocked content Icon in the IE address bar would be helpful."
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: 'Returns the user''s do-not-track setting. This is &quot;yes&quot; if the user has requested not to be tracked by web sites, content, or advertising.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/doNotTrack

---
## Summary

Returns the user's do-not-track setting. This is &quot;yes&quot; if the user has requested not to be tracked by web sites, content, or advertising.

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.doNotTrack;
```

## Return Value

Returns an object of type

Note that navigator.doNotTrack is not the value sent for the do-not-track header. When the do-not-track header sends "1", navigator.doNotTrack is "yes". When the header is unset, navigator.doNotTrack is "unspecified". When the header sends "0" (currently unsupported in Firefox), navigator.doNotTrack is "no".

## Usage

     Could be used to determine if the client web browser may be blocking some page content.

In MSIE browsers when ActiveX content or other content is blocked an Icon is displayed in the Address bar which the user can click to disable Tracking Protection and/or ActiveX filtering for the current site.

## Notes

IE9 uses a vendor prefix, eg. navigator.msDoNotTrack

IE9, Opera 12, Safari 5.1, and Chrome 31 are based on an earlier version of this specification where navigator.doNotTrack is the value sent for the do-not-track header.

IE10 and higher do not use the doNotTrack header which is user configured from the Advanced tab of Internet Options. There is no navigator.doNotTrack or navigator.msdoNotTrack property in those MSIE versions.

### Standards information

The current [Tracking Preference Expression](http://www.w3.org/TR/tracking-dnt/) (Working Draft) is based on an earlier version of this specification where navigator.doNotTrack is the value sent for the do-not-track header.

## See also

### Related pages

-   Internet Explorer Blog: Introducing Tracking Protection[Internet Explorer Blog: Introducing Tracking Protection](http://go.microsoft.com/fwlink/p/?LinkId=212756)
