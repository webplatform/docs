{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example sends an empty message to a server of your choice. You can select a [[apis/xhr/properties/timeout|'''timeout''']] value (default 10000 msec) when sending the request. When you click the '''Get''' button, the script creates a '''XDomainRequest''', assigns event handlers, and initiates the request. Script alerts indicate how the request is progressing. Click the '''Stop''' button to cancel the request, or the '''Read''' button to view additional properties of the response, such as '''contentType''' and '''responseText'''.
|Code=&lt;html&gt;
&lt;script type{{=}}"text/javascript"&gt;
    var xdr;
    function readdata()
    {
        var dRes {{=}} document.getElementById('dResponse');
        dRes.innerText {{=}} xdr.responseText;
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
        var url {{=}} document.getElementById('tbURL');
        var timeout {{=}} document.getElementById('tbTO');
        if (window.XDomainRequest)
        {
            xdr {{=}} new XDomainRequest();
            if (xdr)
            {
                xdr.onerror {{=}} err;
                xdr.ontimeout {{=}} timeo;
                xdr.onprogress {{=}} progres;
                xdr.onload {{=}} loadd;
                xdr.timeout {{=}} tbTO.value;
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
&lt;/script&gt;
&lt;body&gt;
    &lt;h2&gt;XDomainRequest&lt;/h2&gt;
    &lt;input type{{=}}"text" id{{=}}"tbURL" value{{=}}"http://www.contoso.com/xdr.txt" style{{=}}"width:300px"&gt;&lt;br&gt;
    &lt;input type{{=}}"text" id{{=}}"tbTO" value{{=}}"10000"&gt;&lt;br&gt;
    &lt;input type{{=}}"button" onclick{{=}}"mytest()" value{{=}}"Get"&gt;&amp;nbsp;&amp;nbsp;&amp;nbsp;
    &lt;input type{{=}}"button" onclick{{=}}"stopdata()" value{{=}}"Stop"&gt;&amp;nbsp;&amp;nbsp;&amp;nbsp;
    &lt;input type{{=}}"button" onclick{{=}}"readdata()" value{{=}}"Read"&gt;
    &lt;br&gt;
    &lt;div id{{=}}"dResponse"&gt;&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''XDomainRequest''' object is a safe, reliable, and lightweight data service that allows script on any document to anonymously connect to any server and exchange data. Developers can use the '''XDomainRequest''' object when cross-site security is not an issue.
'''Security Warning:  '''
Cross-domain requests ("XDRs") are anonymous to protect user data. This means that servers cannot easily determine who is requesting data. To protect user privacy, respond with cross-domain data that is neither sensitive nor personally identifiable. To help prevent intranet data from being leaked to malicious Internet sites, we discourage intranet sites from making XDR data available.
Cross-domain requests require mutual consent between the document and the server. You can initiate a cross-domain request by creating an '''XDomainRequest''' (XDR) object with the '''window''' object,	and opening a connection to a  domain.
The document will request data from the domain's server by sending an '''Origin''' header with the value of the origin. It will only complete the connection if the server responds with an '''Access-Control-Allow-Origin''' header of either '''*''' or the exact URL of the requesting document. This behavior is part of the World Wide Web Consortium (W3C)'s Web Application Working Group's draft framework on client-side cross-domain communication that the '''XDomainRequest''' object integrates with.
For example, a server's Active Server Pages (ASP) page might include the following response header:
 <code>&lt;% Response.AddHeader("Access-Control-Allow-Origin","*") %&gt;</code>
Cross domain requests can only be sent and received from a document to URLs in the following  zones:
{| class="wikitable"
|-
|From Document \ To URL
!Intranet
!Trusted(Intranet)
!Trusted(Internet)
!Internet
!Restricted
|-
!Intranet
|Allow
|Allow
|Allow
|Allow
|Deny
|-
!Trusted(Intranet)
|Allow
|Allow
|Allow
|Allow
|Deny
|-
!Trusted(Internet)
|Deny
|Deny
|Allow
|Allow
|Deny
|-
!Internet
|Deny
|Deny
|Allow
|Allow
|Deny
|-
!Restricted
|Deny
|Deny
|Deny
|Deny
|Deny
|}
 
The XDR protocol only works with the http:// and https:// protocols.
To use the XDR protocol, you first create an '''XDomainRequest''' object.  
Then you use the '''open''' method to establish a connection with a server. 
Once a connection is opened, the '''send''' method transmits data strings to the server for processing. For example:
 <code>  
 // 1. Create XDR object 
 var xdr {{=}} new XDomainRequest(); 
 // 2. Open connection with server using GET method
 xdr.open("get", "http://www.contoso.com/xdr.aspx");
 // 3. Send string data to server
 xdr.send();     
                 </code>
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>window</code>
*<code>XMLHttpRequest</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}