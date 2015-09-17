---
title: 'item'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/FileList
    href: /apis/file/FileList
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/file/FileList
standardization_status: 'W3C Working Draft'
summary: 'item returns the indexth File object in the FileList. If there is no indexth File object in the FileList, then this method must return null.'
tags:
  - API_Object_Methods
  - API
  - FileAPI
uri: apis/file/FileList/item

---
## Summary

item returns the indexth File object in the FileList. If there is no indexth File object in the FileList, then this method must return null.

Method of [apis/file/FileList](/apis/file/FileList)[apis/file/FileList](/apis/file/FileList)

## Syntax

``` js
var  = FileList.item(index);
```

## Parameters

### index

 Data-type
:   unsigned long

 The [FileList](/apis/file/FileList) index (starting from 0) of the [File](/apis/file/File) object to return.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

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

The first [**File**](/apis/file/File) object in a [**list of files**](/apis/file/FileList) called `selectedFiles` can be accessed by either of the following methods:

-   `selectedFiles.item(0)`
-   `selectedFiles[0]`

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
