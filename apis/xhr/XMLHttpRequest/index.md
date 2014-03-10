{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|XMLHttpRequest allows JavaScript to make HTTP requests, and is the most basic part of AJAX. It allows a website to dynamically request more content, without reloading the entire page.}}
{{API_Object
|Overview=The '''XMLHttpRequest''' property is available on the '''window''' object.
 <code>var xhr {{=}} new XMLHttpRequest();</code>
With the '''XMLHttpRequest''' object, clients can make HTTP requests to a URL without reloading the entire page. Despite the term "XML" in the name, this object can be used to retrieve any type of data.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object. For best client-side performance, the request is asynchronous and uses an '''onreadystatechange''' event handler to process the data returned by the call.
|Code=function handler() {
  if (xhr.readyState {{=}}{{=}}{{=}} 4 /* complete */) {
    if (xhr.status {{=}}{{=}}{{=}} 200) {
            console.log(xhr.responseText);
        }
    }
}
var xhr {{=}} new XMLHttpRequest();
xhr.open("GET", "<nowiki>http://localhost/test.xml</nowiki>", true);
xhr.onreadystatechange {{=}} handler;
xhr.send();
}}{{Single Example
|Language=JavaScript
|Description=This script demonstrates how to access resources that sits on a different domain. 
Example: siteA.com gets resource from siteB.com
|Code=// Create the XHR object.
function createCORSRequest(method, url) {
  var xhr = new XMLHttpRequest();
  if ("withCredentials" in xhr) {
    // XHR for Chrome/Firefox/Opera/Safari.
    xhr.open(method, url, true);
  } else if (typeof XDomainRequest != "undefined") {
    // XDomainRequest for IE 9 and earlier.
    xhr = new XDomainRequest();
    xhr.open(method, url);
  } else {
    // CORS not supported.
    xhr = null;
  }
  return xhr;
}

// Helper method to parse the title tag from the response.
function getTitle(text) {
  return text.match('<title>(.*)?</title>')[1];
}

// Make the actual CORS request.
function makeCorsRequest() {
  // All HTML5 Rocks properties support CORS.
  var url = 'http://updates.html5rocks.com';

  var xhr = createCORSRequest('GET', url);
  if (!xhr) {
    alert('CORS not supported');
    return;
  }

  // Response handlers.
  xhr.onload = function() {
    var text = xhr.responseText;
    var title = getTitle(text);
    alert('Response from CORS request to ' + url + ': ' + title);
  };

  xhr.onerror = function() {
    alert('Woops, there was an error making the request.');
  };

  xhr.send();
}
}}
}}
{{Notes_Section
|Usage=The XMLHttpRequest object can be used to make either same-origin or cross-origin requests.

Same-origin requests are subject to the browser's same-origin policy: http://en.wikipedia.org/wiki/Same_origin_policy  This basically says that an XMLHttpRequest instance can make a request to a resource that lives on the same origin as the calling page.

Requests that go across origins (for example, a request from originA.com to originB.com) can also be made. But in order for them to work, the destination server must support Cross-Origin Resource Sharing (CORS,  http://www.w3.org/TR/cors/). These are a set of headers included in the response that indicate how a resource can be accessed across domains.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C XMLHttpRequest Specification
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=W3C Working Draft
}}{{Related Specification
|Name=Cross-Origin Resource Sharing
|URL=http://www.w3.org/TR/cors/
|Status=W3C Candidate Recommendation 29 January 2013
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=7.0
|Chrome_prefixed_supported=Unknown
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=Unknown
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18.0
|Firefox_mobile_prefixed_supported=Unknown
|IE_mobile_supported=Unknown
|IE_mobile_prefixed_supported=Unknown
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mini_supported=No
|Opera_mini_prefixed_supported=Unknown
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=XHR
}}
{{Topics|XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/cors/
}}