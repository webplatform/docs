---
title: length
tags:
  0: API
  1: Object
  2: Properties
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'length returns the number of files in the FileList object. If there are no files, this attribute must return 0.'
uri: apis/file/FileList/length

---
# length

## Summary

length returns the number of files in the FileList object. If there are no files, this attribute must return 0.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/file/FileList](/apis/file/FileList)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = FileList.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

This example lets you select one or more files, then uses the filelist length to report each filelist item's name and last modified date/time.

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
   alert(filelist.item(i).name + " was last modified: " + filelist.item(i).lastModifiedDate);
 }
```

} \</script\>

</pre>

## Notes

Returns the number of files that are selected and available on the [**FileList**](/apis/file/FileList) object. This value can be greater than or equal to 1 if multiple file selection is enabled (typically via the `multiple` attribute on the `input` element). If no files have been selected, 0 is returned.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

