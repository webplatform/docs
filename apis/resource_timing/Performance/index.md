{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Provides methods for performance timing.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following script calculates the amount of time it takes to fetch every resource in the page, even those defined in markup:
|Code=<!doctype html>
<html>
  <head>
  </head>
  <body onload="loadResources()">
    <script>
       function loadResources() 
       {
          var image1 = new Image();
          image1.src = 'http://w3c-test.org/webperf/image1.png';
          image1.onload = resourceTiming;
       }
       
       function resourceTiming() 
       {
           var resourceList = window.performance.getEntriesByType("resource");
           for (i = 0; i < resourceList.length; i++)
           {
              if (resourceList[i].initiatorType == "img") 
              {
                 alert("End to end resource fetch: "+ resourceList[i].responseEnd - resourceList[i].startTime);
              }
           }
       }
    </script>
    <img id="image0" src="http://w3c-test.org/webperf/image0.png">
  </body>
</html>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing/#extensions-performance-interface
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
{{Topics|API, Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}