---
title: download
notes:
  - 'Compatibility table; link examples to our code.webplatform.org playground; fix see also;'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies that the target item is to be downloaded for offline viewing.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/download

---
## <span>Summary</span>

Specifies that the target item is to be downloaded for offline viewing.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
<http://docs.webplatform.org/wiki/html/elements/a>

</td>
</tr>
</table>
If the download attribute is specified on the [anchor](/html/elements/a) or [area](/html/elements/area) elements, then the browser will attempt to download the item for viewing later. You can optionally give the attribute a value, which will then have the browser store that file with that filename overriding the resources default name.

## <span>Examples</span>

``` html
<!doctype html>
<title>Download attribute demo</title>
<!-- With the download attribute set and having a value the browser will attempt to save the file as the attribute name, overriding the default resource name of "video.mp4". -->
<a href="http://example.com/path/to/video.mp4" download="Web Platform Introduction.mp4">Download the WPD Introduction Video</a>
```

## <span>Related specifications</span>

[HTML5](http://www.w3.org/TR/html5/links.html#downloading-resources)
:   Candidate Recommendation
