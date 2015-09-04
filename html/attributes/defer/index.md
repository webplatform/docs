---
title: defer
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Sets or retrieves the status of the script.'
uri: html/attributes/defer

---
# defer

## Summary

Sets or retrieves the status of the script.

Applies to
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Using the attribute at design time can improve the download performance of a document because the client does not need to parse and execute the script and can continue downloading and parsing the document instead.

### Issues

IE\<10 may interleave execution of scripts. [Discussion on Github.](https://github.com/h5bp/lazyweb-requests/issues/42)

Combining scrips both standard and with `defer` that depend on each other. [Discussion on Github.](https://github.com/zenorocha/browser-diet/issues/95#issuecomment-14852531)

## See also

### Other articles

[http://caniuse.com/\#feat=script-defer](http://caniuse.com/#feat=script-defer)

### Related pages (MSDN)

-   `script`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

