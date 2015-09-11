---
title: name
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/file/File
    href: /apis/file/File
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/file/File
standardization_status: 'W3C Working Draft'
summary: 'The name of the file; on getting, this must return the name of the file as a string. There are numerous file name variations on different systems; this is merely the name of the file, without path information. On getting, if user agents cannot make this information available, they must return the empty string.'
tags:
  0: API
  1: Object
  2: Properties
  4: FileAPI
uri: apis/file/File/name

---
## <span>Summary</span>

The name of the file; on getting, this must return the name of the file as a string. There are numerous file name variations on different systems; this is merely the name of the file, without path information. On getting, if user agents cannot make this information available, they must return the empty string.

Property of [apis/file/File](/apis/file/File)[apis/file/File](/apis/file/File)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = File.name;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

This example lets you select one or more files, then reports each file's name and last modified date/time.

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
    alert(filelist[i].name + " was last modified: " + filelist[i].lastModifiedDate);
  }
}
</script>
```

## <span>Notes</span>

This property returns the name of the file as a string. There are numerous file name variations on different systems; this property is merely the name of the file, without path information. If the file name cannot be obtained, `name` contains an empty string.

## <span>Related specifications</span>

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
