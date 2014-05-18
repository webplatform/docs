{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|Provides a Storage object for an origin, that remains persistent even after restarting the browser. The storage can be cleared by the user with browser functionalities}}
{{API_Object_Property
|Property_applies_to=apis/web-storage/Storage
|Read_only=Yes
|Example_object_name=object
|Javascript_data_type=Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=if (window.localStorage) { // checks if browser support localStorage
  if (localStorage['testKey']) { // checks if value exists
    console.log('Value exist on page load in localstorage for key testKey : ', localStorage['testKey']);
  }
  localStorage['testKey'] = 'Hi again!'; // stores value in localstorage
}
else {
 console.log('your browser dont support localstorage');
}
}}{{Single Example
|Language=HTML
|Description=Fields and buttons for saving, reading and clearing localStorage items.
|Code=<section>
    <label for="key">Key:</label>
    <input type="text" id="key" value="r2d2">
    <br>
    <label for="value">Value:</label>
    <input type="text" id="value" value="C-3PO">
    <br>
    <button type="button" id="set-local">Save to localStorage</button>
</section>
<hr>
<section>
    <label for="get-key">Key:</label>
    <input type="text" id="get-key" value="r2d2">
    <button type="button" id="get-local">Get from localStorage</button>
    <output id="output"></output>
</section>
<hr>
<section>
    <button type="button" id="clear">Clear localStorage</button>
</section>
|LiveURL=http://jsfiddle.net/DM6hB/6/
}}{{Single Example
|Language=JavaScript
|Description=Functions and event handlers for saving, reading and clearing localStorage items.
|Code=/* global document, window */

var valueSetHandler = function () {
    /** read the values from the form */
    var key = document.getElementById('key').value,
        value = document.getElementById('value').value;

    /** save value under key in localStorage */
    window.localStorage.setItem(key, value);
},
valueGetHandler = function () {
    /** read the value from the form */
    var key = document.getElementById('get-key').value,

        /** read the value from the localStorage */
        value = window.localStorage.getItem(key);

    /** write the value in output */
    document.getElementById('output').innerText = value;
},
clearStorageHandler = function () {
    window.localStorage.clear();
};

/** register event Listeners for button clicks */
document.getElementById('set-local').addEventListener('click', valueSetHandler);
document.getElementById('get-local').addEventListener('click', valueGetHandler);
document.getElementById('clear').addEventListener('click', clearStorageHandler);
|LiveURL=<!-- Fields to store a key/value pair (item) in localStorage --> <section>     <label for="key">Key:</label>     <input type="text" id="key" value="r2d2">     <br>     <label for="value">Value:</label>     <input type="text" id="value" value="C-3PO">     <br>     <button type="button" id="set-local">Save to localStorage</button> </section> <hr> <!-- Fields to get a key/value pair (item) from localStorage --> <section>     <label for="get-key">Key:</label>     <input type="text" id="get-key" value="r2d2">     <button type="button" id="get-local">Get from localStorage</button>     <output id="output"></output> </section> <hr> <!-- Button to clear the localStorage for this Domain --> <section>     <button type="button" id="clear">Clear localStorage</button> </section>
}}
}}
{{Notes_Section
|Usage=Use via the methods ''setItem'', ''getItem'', ''removeItem'' and ''clear'' provided by [[apis/web-storage/Storage]]
|Notes=The '''localStorage''' "property" provides an instance of a  storage area object, to which the '''Storage''' object's properties and methods are applied.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}