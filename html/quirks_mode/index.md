---
title: quirks mode
readiness: 'Not Ready'
summary: 'Quirks mode is a way for some browsers to maintain backward compatibility with sites designed for older browsers which don''t strictly comply with W3C or IETF standards.'
tags:
  - API
  - Listings
  - Compatibility
  - Basic
  - Pages
uri: 'html/quirks mode'

---
## Summary

Quirks mode is a way for some browsers to maintain backward compatibility with sites designed for older browsers which don't strictly comply with W3C or IETF standards.

## Notes

When some browser makers implemented CSS, their support did not match W3C standards. To make their sites work correctly with these browsers, developers had to use non-standard CSS.

When standards compliance became more important, developers couldn't switch to standards mode immediately as this would break the sites. Existing CSS would start to show odd side effects when interpreted in the correct way in standards mode.

For example before version 6, IE interpreted the sizing of elements in a web page differently than W3C specifications which led to the infamous "Internet Explorer box model bug". Beginning with IE6, Internet Explorer introduced a second rendering mode (standards mode) but for backward compatiblity issues all versions still behave in the usual, non-standard way by default unless otherwise stated.
