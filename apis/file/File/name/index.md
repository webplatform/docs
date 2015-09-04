---
title: name
tags:
  0: API
  1: Object
  2: Properties
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The name of the file; on getting, this must return the name of the file as a string. There are numerous file name variations on different systems; this is merely the name of the file, without path information. On getting, if user agents cannot make this information available, they must return the empty string.'
uri: apis/file/File/name

---
# name

## Summary

The name of the file; on getting, this must return the name of the file as a string. There are numerous file name variations on different systems; this is merely the name of the file, without path information. On getting, if user agents cannot make this information available, they must return the empty string.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/file/File](/apis/file/File)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = File.name;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

This example lets you select one or more files, then reports each file's name and last modified date/time.

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

} \</script\>

</pre>

## Notes

This property returns the name of the file as a string. There are numerous file name variations on different systems; this property is merely the name of the file, without path information. If the file name cannot be obtained, `name` contains an empty string.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

