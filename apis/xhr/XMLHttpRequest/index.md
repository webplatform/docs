{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|XMLHttpRequest is the most basic part of AJAX. It allows a website to dynamically request more content, without loading the page.}}
{{API_Object
|Overview=The '''XMLHttpRequest''' property is available on the '''window''' object.
 <code>var xhr {{=}} new XMLHttpRequest();</code>
With the '''XMLHttpRequest''' object, clients can retrieve and submit XML data directly to a web server without reloading the document. To convert XML data into renderable HTML content, use the client-side XML DOM or Extensible Stylesheet Language Transformations (XSLT) to compose HTML elements for presentation.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object. For best client-side performance, the request is asynchronous and uses an [[apis/xhr/events/readystatechange|'''onreadystatechange''']] event handler to process the data returned by the call.
|Code=function handler() {
  if (xhr.readyState {{=}}{{=}}{{=}} 4 /* complete */) {
    if (xhr.status {{=}}{{=}}{{=}} 200) {
            console.log(xhr.responseText);
        }
    }
}
var xhr {{=}} new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange {{=}} handler;
xhr.send();
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=XMLHttpRequest
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=Working Draft
|Relevant_changes=Section 3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=Windows Internet Explorer earlier than version 7 does not implement the native XMLHttpRequest object. The XMLHTTP ActiveX object emulates the same functionality. While the native XMLHttpRequest object also supports the use of expandos (custom properties) and properly recognizes the 'this' notation of JavaScript, the ActiveX version does not. To support versions of Windows Internet Explorer prior to Internet Explorer 7, use the following function to get the '''XMLHttpRequest''' object.  <code>function getXMLHttpRequest()   {      if (window.XMLHttpRequest) {          return new window.XMLHttpRequest;      }      else {          try {              return new ActiveXObject("MSXML2.XMLHTTP.3.0");          }          catch (ex) {              return null;          }      }  }</code>
}}
}}
{{See_Also_Section}}
{{Topics|DOM, XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}