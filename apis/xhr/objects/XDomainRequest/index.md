---
title: XDomainRequest
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - API
  - Objects
  - DOM
uri: apis/xhr/objects/XDomainRequest

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

API Name
:   Summary

[open (XDomainRequest)](/apis/xhr/methods/open_(XDomainRequest))
:

[send (XDomainRequest)](/apis/xhr/methods/send_(XDomainRequest))
:

## <span>Events</span>

*No events.*

## <span>Examples</span>

The following example sends an empty message to a server of your choice. You can select a [**timeout**](/apis/xhr/events/timeout) value (default 10000 msec) when sending the request. When you click the **Get** button, the script creates a **XDomainRequest**, assigns event handlers, and initiates the request. Script alerts indicate how the request is progressing. Click the **Stop** button to cancel the request, or the **Read** button to view additional properties of the response, such as **contentType** and **responseText**.

``` html
<html>
<script type="text/javascript">
    var xdr;
    function readdata()
    {
        var dRes = document.getElementById('dResponse');
        dRes.innerText = xdr.responseText;
        alert("Content-type: " + xdr.contentType);
        alert("Length: " + xdr.responseText.length);
    }

    function err()
    {
        alert("XDR onerror");
    }
    function timeo()
    {
        alert("XDR ontimeout");
    }
    function loadd()
    {
        alert("XDR onload");
        alert("Got: " + xdr.responseText);
    }
    function progres()
    {
        alert("XDR onprogress");
        alert("Got: " + xdr.responseText);
    }
    function stopdata()
    {
        xdr.abort();
    }
    function mytest()
    {
        var url = document.getElementById('tbURL');
        var timeout = document.getElementById('tbTO');
        if (window.XDomainRequest)
        {
            xdr = new XDomainRequest();
            if (xdr)
            {
                xdr.onerror = err;
                xdr.ontimeout = timeo;
                xdr.onprogress = progres;
                xdr.onload = loadd;
                xdr.timeout = tbTO.value;
                xdr.open("get", tbURL.value);
                xdr.send();
            }
            else
            {
                alert('Failed to create');
            }
        }
        else
        {
            alert('XDR doesn't exist');
        }
    }
</script>
<body>
    <h2>XDomainRequest</h2>
    <input type="text" id="tbURL" value="http://www.contoso.com/xdr.txt" style="width:300px"><br>
    <input type="text" id="tbTO" value="10000"><br>
    <input type="button" onclick="mytest()" value="Get">&nbsp;&nbsp;&nbsp;
    <input type="button" onclick="stopdata()" value="Stop">&nbsp;&nbsp;&nbsp;
    <input type="button" onclick="readdata()" value="Read">
    <br>
    <div id="dResponse"></div>
</body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

The **XDomainRequest** object is a safe, reliable, and lightweight data service that allows script on any document to anonymously connect to any server and exchange data. Developers can use the **XDomainRequest** object when cross-site security is not an issue. **Security Warning:  ** Cross-domain requests ("XDRs") are anonymous to protect user data. This means that servers cannot easily determine who is requesting data. To protect user privacy, respond with cross-domain data that is neither sensitive nor personally identifiable. To help prevent intranet data from being leaked to malicious Internet sites, we discourage intranet sites from making XDR data available. Cross-domain requests require mutual consent between the document and the server. You can initiate a cross-domain request by creating an **XDomainRequest** (XDR) object with the **window** object, and opening a connection to a domain. The document will request data from the domain's server by sending an **Origin** header with the value of the origin. It will only complete the connection if the server responds with an **Access-Control-Allow-Origin** header of either **\*** or the exact URL of the requesting document. This behavior is part of the World Wide Web Consortium (W3C)'s Web Application Working Group's draft framework on client-side cross-domain communication that the **XDomainRequest** object integrates with. For example, a server's Active Server Pages (ASP) page might include the following response header:

    <% Response.AddHeader("Access-Control-Allow-Origin","*") %>

Cross domain requests can only be sent and received from a document to URLs in the following zones: {

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `window`
-   `XMLHttpRequest`
