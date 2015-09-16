---
title: 'FileReader'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[FileReader](https://developer.mozilla.org/en-US/docs/Web/API/FileReader) Article]'
  - 'Microsoft Developer Network: [[fileReader Object](http://msdn.microsoft.com/en-us/library/ie/hh772310(v=vs.85).aspx) Article]'
code_samples:
  - 'https://developer.mozilla.org/files/3698/image_upload_preview.html'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'The FileReader object lets web applications asynchronously read the contents of files (or raw data buffers) stored on the user''s computer, using File or Blob objects to specify the file or data to read. File objects may be obtained from a FileList object returned as a result of a user selecting files using the input element, from a drag-and-drop operation''s DataTransfer object, or from the mozGetAsFile() API on an HTMLCanvasElement.'
tags:
  0: API
  1: Objects
  3: FileAPI
uri: apis/file/FileReader

---
## Summary

The FileReader object lets web applications asynchronously read the contents of files (or raw data buffers) stored on the user's computer, using File or Blob objects to specify the file or data to read. File objects may be obtained from a FileList object returned as a result of a user selecting files using the input element, from a drag-and-drop operation's DataTransfer object, or from the mozGetAsFile() API on an HTMLCanvasElement.

## Properties

*No properties.*

## Methods

API Name
:   Summary

[abort](/apis/file/FileReader/abort)
:   The abort method is used to aborts the read operation. Upon return, the [dom/Element/readyState](/dom/Element/readyState) will be *DONE*.

[readAsArrayBuffer](/apis/file/FileReader/readAsArrayBuffer)
:   Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), as an ArrayBuffer object, a fixed-length binary data buffer.

[readAsDataURL](/apis/file/FileReader/readAsDataURL)
:   Returns the complete data of blob as a Data URL, essentially a Base64-encoded string of the file data.

[readAsText](/apis/file/FileReader/readAsText)
:   Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), decoded into memory according to the encoding determination.

## Events

*No events.*

## Examples

Preview an image before upload

``` html
<!doctype html>
<html>
<head>
<meta content="text/html; charset=UTF-8" http-equiv="Content-Type" />
<title>Image preview example</title>
<script type="text/javascript">
oFReader = new FileReader(), rFilter = 'image/jpg';

oFReader.onload = function (oFREvent) {
  document.getElementById("uploadPreview").src = oFREvent.target.result;
};

function loadImageFile() {
  if (document.getElementById("uploadImage").files.length === 0) { return; }
  var oFile = document.getElementById("uploadImage").files[0];
  if (!rFilter.test(oFile.type)) { alert("You must select a valid image file!"); return; }
  oFReader.readAsDataURL(oFile);
}
</script>
</head>

<body onload="loadImageFile();">
  <form name="uploadForm">
    <table>
      <tbody>
        <tr>
          <td><img id="uploadPreview" style="width: 100px; height: 100px;" src="" alt="Image preview" /></td>
          <td><input id="uploadImage" type="file" name="myPhoto" onchange="loadImageFile();" /></td>
        </tr>
      </tbody>
    </table>

    <p><input type="submit" value="Send" /></p>
  </form>
</body>
</html>
```

[View live example](https://developer.mozilla.org/files/3698/image_upload_preview.html)

## Notes

When the `FileReader` constructor is invoked, a new FileReader object is returned. This FileReader object enables asynchronous reads on individual File objects by firing progress events as the read occurs to event handler methods attached to the FileReader object.

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## See also

### Other articles

[Using files from web applications](https://developer.mozilla.org/en-US/docs/Using_files_from_web_applications)
