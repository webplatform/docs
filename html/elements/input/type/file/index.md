---
title: file
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The file type of the &lt;input&gt; element represents widget for specifying a file.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'dom/properties/value (type/file) B685'
uri: html/elements/input/type/file

---
## Summary

The file type of the &lt;input&gt; element represents widget for specifying a file.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

The following example lets the user choose one or more files, and then displays the choices. The files list can also be used to upload to a website.

``` html
<!DOCTYPE html>
<html >
<head>
<title>Files property test</title>
<script type="text/javascript">
  function getFiles() {
    // Get input element
    myFileList = document.getElementById("myfiles");
    // loop through files property, using length to get number of files chosen
    for (var i = 0; i < myFileList.files.length; i++) {
        // display them in the div
        document.getElementById("display").innerHTML += "<br/>" + myFileList.files[i].name ;
    }
  }
</script>
</head>
<body>
<label>Use <strong>shift</strong> or <strong>ctrl</strong> click to pick a few files:
<input type="file" multiple id="myfiles" onchange="getFiles();" /></label>
<div id="display"></div>
</body>
</html>
```

use the input file type to upload a file to a server

``` html
<form name="oForm"
   action="/endpoint"
   enctype="multipart/form-data"
   method="post">
<input type="file" name="oFile1"/>
<input type="submit" value="Upload File">
</form>
```

## Notes

### Remarks

For a file upload to take place:

-   The **INPUT type=file** element must be enclosed within a **FORM** element.
-   A value must be specified for the [**NAME**](/html/attributes/name) attribute of the **INPUT type=file** element.
-   The [**METHOD**](/html/attributes/method) attribute of the **FORM** element must be set to **post**.
-   The [**ENCTYPE**](/html/attributes/encoding) attribute of the **FORM** element must be set to multipart/form-data.

**Note**  For code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site. To handle a file upload to the server, a server-side process must be running that can handle multipart/form-data submissions. For example, the Microsoft Posting Acceptor allows Microsoft Internet Information Server (IIS) to accept file uploads. Additional Common Gateway Interface (CGI) scripts that can handle multipart/form-data submissions are available on the Web.

Windows Internet Explorer 8 and later. When a file is selected by using the **input type=file** object, the value of the [**value**](/w/index.php?title=dom/properties/value_(type/file)_B685&action=edit&redlink=1) property depends on the value of the "Include local directory path when uploading files to a server" security setting for the security zone used to display the Web page containing the **input** object. For more information, see [**value**](/w/index.php?title=dom/properties/value_(type/file)_B685&action=edit&redlink=1). Windows Internet Explorer 7 and later. By default, Internet Explorer does not include folder or directory path information when uploading files to sites in the Restricted zone. This improves security by preventing information disclosure. Also, to improve accessibility, the **INPUT type=file** element now contains two accessible elements—one for the input box and one for the **Browse** button. This change is applicable only to accessibility tools; script implementations are not affected. Microsoft Internet Explorer 6 for Windows XP Service Pack 2 (SP2) and later. For security reasons, the **input type=file** element no longer accepts relative file paths. Microsoft Internet Explorer raises an Access Denied exception when the user attempts to submit a form containing an **input type=file** element that contains a relative path. The **INPUT type=file** element is available in HTML and script as of Microsoft Internet Explorer 4.0. The file upload add-on is required to use the **INPUT type=file** element in Microsoft Internet Explorer 3.02. Users can enter a file path in the text box or click the **Browse** button to browse the file system. When a file is uploaded, the file name is also submitted.

### Compatibility notes

Firefox for Android sets a default `border` on `<input type="file">` elements, unlike most other browsers.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10

### HTML information

<table class="wikitable">
<tr>
<th>
Closing Tag

</th>
<td>
forbidden

</td>
</tr>
<tr>
<th>
CSS Display

</th>
<td>
inline

</td>
</tr>
</table>
### Members

The **input type=file** object has these types of members:

-   [\#events Events]
-   [\#methods Methods]
-   [\#properties Properties]

#### Events

The **input type=file** object has these events. {
