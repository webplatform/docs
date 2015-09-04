---
title: lastModifiedDate
tags:
  0: API
  1: Object
  2: Properties
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The last modified date of the file. On getting, if user agents can make this information available, this must return a new Date object initialized to the last modified date of the file. If the last modification date and time are not known, the attribute must return the current date and time as a Date object.'
uri: apis/file/File/lastModifiedDate

---
# lastModifiedDate

## Summary

The last modified date of the file. On getting, if user agents can make this information available, this must return a new Date object initialized to the last modified date of the file. If the last modification date and time are not known, the attribute must return the current date and time as a Date object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/file/File](/apis/file/File)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = File.lastModifiedDate;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

This example lets you select one or more files, then reports each file's name and last modified date/time.

``` {.html}
<input type="file" multiple id="myfileinput">
<input type="button" value="Show file names and last modified dates" onclick="shownd()">
. . .
<script>
function shownd() {

 var fileinp = document.getElementById("myfileinput");
 var filelist = fileinp.files;
 alert(filelist.length);
 for (var i = 0; i < filelist.length; i++) {
   alert(filelist[i].name + " was last modified: " + filelist[i].lastModifiedDate);
 }
```

} \</script\>

</pre>

## Notes

Returns the last modified date of the file in the form of a new **Date** object. If the browser can't obtain file date information, null is returned.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

