---
title: 'Introduction to MIME types'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Properly_Configuring_Server_MIME_Types)'
readiness: 'Ready to Use'
summary: 'MIME types enable browsers to recognize the filetype of a file which has been sent via HTTP by the webserver. As a result the browser is able to choose a suitable displaying method. Common MIME types are for example text/html for html-files or image/jpeg for jpeg-files.'
tags:
  - Concept_Pages
  - Web_Services
uri: 'concepts/Internet and Web/mime types'

---
## Summary

MIME types enable browsers to recognize the filetype of a file which has been sent via HTTP by the webserver. As a result the browser is able to choose a suitable displaying method. Common MIME types are for example text/html for html-files or image/jpeg for jpeg-files.

#### original by Bob Clary

#### published Feb. 20, 2003

## What are MIME types?

MIME (Multi-purpose Internet Mail Extensions) is an expansion of the original Internet e-mail protocol that exchanges different kinds of data files on the Internet: text, audio, video, images, application programs, and others. In 1991, the protocol was extended so that Internet clients and servers could recognize and handle various kinds of data, and new file types were added to the "mail" protocol as supported Internet Protocol file types.

Servers insert the MIME header at the beginning of any web transmission. Clients use this header to select an appropriate display, or "player", application for the type of data indicated by the header. Some of these players are built into the client, typically a browser (for example, all browsers come with GIF and JPEG image players, as well as the ability to handle HTML files); other players may need to be downloaded.

MIME types—also sometimes called Internet media types or Content-types—describe the media type of content either contained in email or served by web servers or web applications, and are intended to help guide a web browser to correctly process and display the content. Examples of MIME types are:

-   `text/html` for normal web pages
-   `text/plain` for plain text
-   `application/octet-stream` meaning "download this file"
-   `application/x-java-applet` for Java<sup>™</sup> applets
-   `application/pdf` for Adobe<sup>®</sup> PDF documents.

By default, many web servers are configured to report a MIME type of `text/plain` or `application/octet-stream` for unknown content types. As new content types are invented or added to web servers, web administrators may fail to add the new MIME types to their web server's configuration. This is a major source of problems for users of Gecko-based browsers, which respect the MIME types as reported by web servers and web applications.

### Technical Background

MIME is currently defined in RFCs [2045](http://www.isi.edu/in-notes/rfc2045.txt), [2046](http://www.isi.edu/in-notes/rfc2046.txt), [2047](http://www.isi.edu/in-notes/rfc2047.txt), [2048](http://www.isi.edu/in-notes/rfc2048.txt), and [2049](http://www.isi.edu/in-notes/rfc2049.txt); registered values for MIME types are available in [IANA/MIME Media Types](http://www.iana.org/assignments/media-types/index.html). The [HTTP specification](http://www.w3.org/Protocols/HTTP/1.1/spec.html) defines a superset of MIME which is used to describe the media types used on the web.

## Why are correct MIME types important?

If the web server or application reports an incorrect MIME type for content, a web browser has no way, *according to the HTTP specification*, of knowing that the author actually intended the content to be processed and displayed in a way different from that implied by the reported MIME type.

Some other web browsers, such as Internet Explorer, try to allow for misconfigured web servers and applications by *[guessing](http://support.microsoft.com/default.aspx?sd=msdn&scid=kb;en-us;293336)* what the correct MIME type should be. This has sheltered many web administrators from their own errors as, using this method, Internet Explorer will continue to process content as expected even though the web server is misconfigured, e.g., it may correctly display an image that is reported to be plain text.

Serving content using the correct MIME type can also be important for security reasons; it's possible for malicious content to affect the user's computer by pretending to be a safe type of document when it is in fact not.

### Why browsers should not guess MIME types

Apart from violating the HTTP specification, it is a bad strategy for browsers to guess MIME types for the following reasons.

#### Loss of control

If the browser ignores the reported MIME type, web administrators and authors no longer have control over how their content is to be processed.

For example, a website oriented for web developers might wish to send certain example HTML documents as either `text/html` or `text/plain` in order to have the documents either processed and displayed as HTML or as source code. If the browser guesses the MIME type, this option is no longer available to the author.

#### Security

Some content types, such as executable programs, are inherently unsafe. For this reason, the actions a browser can take when given content of that type are usually restricted. For example, an executable program should not be executed on the user's computer, and at most should cause a dialog to appear asking the user if they wish to download the file.

MIME type guessing has led to security exploits in Internet Explorer based on malicious authors incorrectly reporting a MIME type of a dangerous file as a safe type. This deliberate misrepresentation bypassed the normal download dialog, resulting in Internet Explorer correctly guessing that the content was an executable program and then running it on the user's computer.

## How to determine the MIME type sent by a server

In Firefox, load the file and use `Tools > Page Info`. You can also use [Rex Swain's HTTP Viewer](http://www.rexswain.com/httpview.html) or [Live HTTP Headers](http://livehttpheaders.mozdev.org/) to see the full headers and content of any file sent from a web server.

According to the standards, a `meta` tag that gives the MIME type such as `<meta  http-equiv="Content-Type" content="text/html">` should be ignored if there's a `Content-Type` line in the header. Instead of looking for this line in the HTML source, use the above techniques to determine the MIME type sent by the server.

## How to determine the correct MIME type for your content

There are several steps you can take to determine the correct MIME type value to be used for your content.

1.  If your content was created using a vendor's software application, read the vendor's documentation to see which MIME types should be reported for its media types.
2.  Look in the [IANA/MIME Media Types registry](http://www.iana.org/assignments/media-types/index.html), which contains all registered MIME types.
3.  Search for the file extension at [FILExt](http://filext.com/) or [File extensions reference](http://www.file-extensions.org/) to see what MIME types are associated with that extension.

## Common MIME Types

|MIME Type|File Type|
|:--------|:--------|
|application/javascript|js, jsonp|
|application/json|json|
|application/octet-stream|safariextz|
|application/vnd.ms-fontobject|eot|
|application/x-chrome-extension|crx|
|application/x-font-woff|woff|
|application/x-shockwave-flash|swf|
|application/x-web-app-manifest+json|webapp|
|application/x-xpinstall|xpi|
|application/xml|rss, atom, xml, rdf|
|audio/mp4|m4a, f4a, f4b|
|audio/ogg|ogg, oga|
|font/opentype|otf|
|image/svg+xml|svg, svgz|
|image/webp|webp|
|image/x-icon|ico|
|text/cache-manifest|appcache, manifest|
|text/v-card|vcf|
|text/vtt|vtt|
|text/x-component|htc|
|video/mp4|mp4, m4v, f4v, f4p|
|video/ogg|ogv|
|video/webm|webm|
|video/x-flv|flv|
|x-font-ttf|ttf, ttc|

## Related Links

-   [Incorrect MIME Type for CSS Files](https://developer.mozilla.org/en/Incorrect_MIME_Type_for_CSS_Files)
-   [IANA/MIME Media Types](http://www.iana.org/assignments/media-types/index.html)
-   [Hypertext Transfer Protocol—HTTP/1.1](http://www.w3.org/Protocols/HTTP/1.1/spec.html)
-   [Microsoft - 293336 - INFO: WebCast: MIME Type Handling in Microsoft Internet Explorer](http://support.microsoft.com/default.aspx?sd=msdn&scid=kb;en-us;293336)
-   [Microsoft - Appendix A: MIME Type Detection in Internet Explorer](http://msdn.microsoft.com/workshop/networking/moniker/overview/appendix_a.asp)
-   [Microsoft - Security Update, March 29, 2001](http://www.microsoft.com/windows/ie/downloads/critical/q290108/)
-   [Microsoft - Security Update, December 13, 2001](http://www.microsoft.com/windows/ie/downloads/critical/Q313675/)
