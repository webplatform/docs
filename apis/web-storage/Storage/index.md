{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Key names are exposed as properties on this object. For example, the following statements are equivalent:
|Code=sessionStorage.setItem('myKey', '...');
					
sessionStorage['myKey'] {{=}} '...'; 
	
sessionStorage.myKey {{=}} '...';
}}{{Single Example
|Code=<!DOCTYPE html>
<html>
  <head>
  <style>
    <!-- include CSS -->
  </style>
  </head>
  <body>
    <header>
      <h1>LocalStorage</h1><div class="arrow-right"></div>
      <h2>Saving permanent textarea content</h2>
    </header>  
    <div id="excerpt">
      This sample saves some text on the localStorage object and retrieves the value on load time. Use your browser developer tools to debug the values of the localStorage object.
    </div>
    <div id="content"></div>
    <p id="log"></p>
    <!-- Javscript -->
  </body>
</html>
|LiveURL=http://playground.html5rocks.com/#localstorage
}}{{Single Example
|Language=CSS
|Description=CSS part
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
|Description=Javascript part
|Code=  // Generate the little markup from javascript
      document.querySelector('#content').innerHTML =
          '<p><em>Save text locally (it will still be available after restarting your browser)</em></p>';
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
          delta = ((new Date()).getTime() - (new Date()).setTime(window.localStorage.getItem('timestamp'))) / 1000;
          document.querySelector("#log").innerHTML = 'last saved: ' + delta + 's ago';
        }
        else {
          area.value = 'Type your text here...';
        }
      }
}}
}}
{{Notes_Section
|Notes====Remarks===
Each '''Storage''' object provides access to a list of key/value pairs, which are sometimes called items. Keys are strings, and any string (including the empty string) is a valid key. Items contain values (which are also strings) and associated metadata.
Each '''Storage''' object is associated with a list of key/value pairs when it is created. Multiple '''Storage''' objects, such as two instances of [[apis/web-storage/properties/localStorage|'''localStorage''']], can be associated with the same list of key/value pairs simultaneously.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''HTMLStorage''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''HTMLStorage''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[apis/web-storage/methods/clear|'''clear''']]
|Removes all key/value pairs from the Web Storage area.
|-
|[[apis/web-storage/methods/getItem|'''getItem''']]
|Retrieves the current value associated with the Web Storage key.
|-
|[[apis/web-storage/methods/key|'''key''']]
|Retrieves the key at the specified index in the collection.
|-
|[[apis/web-storage/methods/removeItem|'''removeItem''']]
|Deletes a key/value pair from the Web Storage collection.
|-
|[[apis/web-storage/methods/setItem|'''setItem''']]
|Sets a key/value pair.
|}
 

====Properties====
The '''HTMLStorage''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[apis/web-storage/properties/length|'''length''']]
|Retrieves the length of the key/value list.
|-
|[[apis/web-storage/properties/remainingSpace|'''remainingSpace''']]
|Retrieves the remaining memory space, in bytes, for the storage object.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/web-storage/properties/localStorage|localStorage]]</code>
}}
{{Topics|DOM, Webstorage}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=http://playground.html5rocks.com/#localstorage
}}