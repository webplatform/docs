---
title: FileList
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[FileList](https://developer.mozilla.org/en-US/docs/DOM/FileList) Article]'
  - 'Microsoft Developer Network: [[fileList Object](http://msdn.microsoft.com/en-us/library/ie/hh772307(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'FileList is an object which represents an array of individually selected files from the underlying system.'
tags:
  0: API
  1: Objects
  3: FileAPI
uri: apis/file/FileList

---
## <span>Summary</span>

FileList is an object which represents an array of individually selected files from the underlying system.

## <span>Properties</span>

API Name
:   Summary

[length](/apis/file/FileList/length)
:   **length** returns the number of files in the FileList object. If there are no files, this attribute must return 0.

## <span>Methods</span>

API Name
:   Summary

[item](/apis/file/FileList/item)
:   **item** returns the *index*th File object in the FileList. If there is no *index*th File object in the FileList, then this method must return null.

## <span>Events</span>

*No events.*

## <span>Examples</span>

iterates over all the files selected by the user using an input element

``` js
// fileInput is an HTML input element: input type="file" id="myfileinput" multiple
var fileInput = document.getElementById("myfileinput");

// files is a FileList object (similar to NodeList)
var files = fileInput.files;
var file;

// loop trough files
for (var i = 0; i < files.length; i++) {

    // get item
    file = files.item(i);
    //or
    file = files[i];

    alert(file.name);
}
```

## <span>Related specifications</span>

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
