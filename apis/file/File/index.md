---
title: 'File'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[File](https://developer.mozilla.org/en-US/docs/Web/API/File) Article]'
  - 'Microsoft Developer Network: [[file Object](http://msdn.microsoft.com/en-us/library/ie/hh772305(v=vs.85).aspx) Article]'
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/file/dndfiles/)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The File object provides information about files stored on the user''s computer, and access to their contents. These are generally retrieved from a FileList object returned when a user selects files using the input element, or from a drag-and-drop operation''s DataTransfer object.'
tags:
  - API_Objects
  - API
  - FileAPI
uri: apis/file/File

---
## Summary

The File object provides information about files stored on the user's computer, and access to their contents. These are generally retrieved from a FileList object returned when a user selects files using the input element, or from a drag-and-drop operation's DataTransfer object.

## Properties

[lastModifiedDate](/apis/file/File/lastModifiedDate)
:   The last modified date of the file. On getting, if user agents can make this information available, this must return a new Date object initialized to the last modified date of the file. If the last modification date and time are not known, the attribute must return the current date and time as a Date object.

[name](/apis/file/File/name)
:   The name of the file; on getting, this must return the name of the file as a string. There are numerous file name variations on different systems; this is merely the name of the file, without path information. On getting, if user agents cannot make this information available, they must return the empty string.

## Methods

*No methods.*

## Events

*No events.*

## Examples

Using form input for selecting files

``` js
function handleFileSelect(evt) {
    var files = evt.target.files; // FileList object

    // files is a FileList of File objects. List some properties.
    var output = [];
    for (var i = 0, f; f = files[i]; i++) {
      output.push(escape(f.name),
                  f.size, ' bytes, last modified: ',
                  f.lastModifiedDate ? f.lastModifiedDate.toLocaleDateString() : 'n/a');
    }
    document.getElementById('list').innerHTML = output.join('');
  }

  document.getElementById('files').addEventListener('change', handleFileSelect, false);
```

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
