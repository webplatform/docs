{{Page_Title}}
{{Flags
|Content=Needs Summary
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Provides access to a list of key/value pairs, sometimes called "items". The amount of storage space is limited by browsers.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Key names are exposed as properties on this object. For example, the following statements are equivalent:
|Code=sessionStorage.setItem('myKey', '...');
					
sessionStorage['myKey'] {{=}} '...'; 
	
sessionStorage.myKey {{=}} '...';
}}{{Single Example
|Language=HTML
|Code=<html>
  <head>
    <style>
    <!-- include CSS -->
    </style>
  </head>

  <body>
      
    <nowiki><div id="example-excerpt">
      This sample saves some text on the localStorage object 
      and retrieves the value on load time. 
      Use your browser developer tools to debug the 
      values of the localStorage object.
    </div></nowiki>

    <nowiki><div id="example-content"></div>

    <p id="log"></p>

    <!-- Javscript -->

  </body></nowiki>
</html>
|LiveURL=http://playground.html5rocks.com/#localstorage
}}{{Single Example
|Language=CSS
|Code=body {
      font: 100% "Lucida Grande", "Trebuchet MS", Verdana, sans-serif;
      margin: 0;
    }
    
    #log {
      background-color: gray;
      color: white;
      padding: 10px;
      margin-left: 20px;
      display: inline-block;
    }
    
    header {
      background: #FFCC99;
      color: white;
      -moz-box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      -webkit-box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      box-shadow: 0 2px 8px -3px rgba(0,0,0,.5), 0 1.4em 2em -0.7em rgba(255, 255, 255, .2) inset;
      text-shadow: 1px 1px 1px #444;
    }
    
    header h1, header h2 {
      display: inline-block;
      padding: 12px 15px;
      font-size: 105%;
      line-height: 1;
      margin: 0;
    }
    
    header h1 {
      background: #FF9966;
    }
    
    #excerpt {
      padding: 20px;
      background: #fcfaea;
    }
    
    .arrow-right {
      display: inline-block;
      width: 0;
      height: 0;
      border-top: 18px solid transparent;
      border-bottom: 18px solid transparent;
      border-left: 18px solid #FF9966;
      margin-bottom: -11px;
    }
    
    #content {
      padding: 20px;
      color: #333;
    }
    
    input, textarea {
      font-size: 100%;
    }
}}{{Single Example
|Language=JavaScript
|Code=// Generate the little markup from javascript 
<nowiki>
document.querySelector('#content').innerHTML =
          '<p><em>Save text locally (it will still be available 
          after restarting your browser)</em></p>';

var area = document.createElement('textarea');
    area.style.width = '300px';
    area.style.height = '150px';
      document.querySelector('#content').appendChild(area);
      
      // place content from previous edit
      if (!area.value) {
        area.value = window.localStorage.getItem('value');
      }
       
      // your content will be saved locally
      area.addEventListener('keyup', function () {
        window.localStorage.setItem('value', area.value);
        window.localStorage.setItem('timestamp', (new Date()).getTime());
      }, false);
      
      updateLog();
      setInterval(updateLog, 5000); // show time every 5 seconds
      
      function updateLog() {
        var delta = 0;
        if (window.localStorage.getItem('value')) {
          delta = ((new Date()).getTime() - 
            (new Date()).setTime(window.localStorage.getItem
            ('timestamp'))) / 1000;
          document.querySelector("#log").innerHTML = 'last saved: ' + delta + 's ago';
        }
        else {
          area.value = 'Type your text here...';
        }
      }</nowiki>
}}
}}
{{Notes_Section
|Notes=Each '''Storage''' object provides access to a list of key/value pairs, which are sometimes called items. Keys are strings, and any string (including the empty string) is a valid key. Items contain values (which are also strings) and associated metadata.

Each '''Storage''' object is associated with a list of key/value pairs when it is created. Multiple '''Storage''' objects, such as two instances of '''localStorage''', can be associated with the same list of key/value pairs simultaneously.
|Import_Notes=The '''amount of storage''' is '''limited''' by the browser (quota). An error is thrown, when the quota is exceeded. 
An example, that intentionally exceeds the quota and throws and error may be found here: http://jsfiddle.net/wkDc6/1/
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Storage Specification
|URL=http://www.w3.org/TR/webstorage/
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Webstorage}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=http://playground.html5rocks.com/#localstorage
}}