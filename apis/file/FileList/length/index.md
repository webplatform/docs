---
title: 'length'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/file/FileList
    href: /apis/file/FileList
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/file/FileList
standardization_status: 'W3C Working Draft'
summary: 'length returns the number of files in the FileList object. If there are no files, this attribute must return 0.'
tags:
  - API_Object_Properties
  - API
  - FileAPI
uri: apis/file/FileList/length

---
## Summary

length returns the number of files in the FileList object. If there are no files, this attribute must return 0.

Property of [apis/file/FileList](/apis/file/FileList)[apis/file/FileList](/apis/file/FileList)

## Syntax

**Note**: This property is read-only.

``` js
var result = FileList.length;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

This example lets you select one or more files, then uses the filelist length to report each filelist item's name and last modified date/time.

``` html
<input type="file" multiple id="myfileinput"><br/>
<input type="button" value="Show file names and last modified dates" onclick="shownd()">
<p>. . .</p>
<script>
function shownd() {
  var fileinp = document.getElementById("myfileinput");
  var filelist = fileinp.files;
  alert(filelist.length);
  for (var i = 0; i < filelist.length; i++) {
    alert(filelist.item(i).name + " was last modified: " + filelist.item(i).lastModifiedDate);
  }
}
</script>
```

## Notes

Returns the number of files that are selected and available on the [**FileList**](/apis/file/FileList) object. This value can be greater than or equal to 1 if multiple file selection is enabled (typically via the `multiple` attribute on the `input` element). If no files have been selected, 0 is returned.

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
