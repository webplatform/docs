{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Provides methods for performance timing.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following JavaScript shows a simple attempt to measure the time it takes to fetch a resource:
|Code=<!doctype html>
<html>
  <head>
  </head>
  <body onload="loadResources()">
    <script>
        function loadResources() 
        {
           var start = new Date().getTime();
           var image1 = new Image();
           image1.src = 'http://w3c-test.org/webperf/image1.png';
           image1.onload = resourceTiming;

           var resourceTiming = function() {
               var now = new Date().getTime();
               var latency = now - start;
               alert("End to end resource fetch: " + latency);
           };
        } 
    </script>
    <img src="http://w3c-test.org/webperf/image0.png">
  </body>
</html>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}