{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|Provides a Storage object for an origin, that remains persistent even after restarting the browser. The storage can be cleared by the user with browser functionalities. If you need a temporary storage, use [[apis/web-storage/Storage/sessionStorage]]}}
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
|Code=<!-- Fields to store a key/value pair (item) in localStorage -->
<section>
    <label for="key">Key:</label>
    <input type="text" id="key" value="r2d2">
    <br>
    <label for="value">Value:</label>
    <input type="text" id="value" value="C-3PO">
    <br>
    <button type="button" id="set-local">Save to localStorage</button>
</section>
<hr>
<!-- Fields to get a key/value pair (item) from localStorage -->
<section>
    <label for="get-key">Key:</label>
    <input type="text" id="get-key" value="r2d2">
    <button type="button" id="get-local">Get from localStorage</button>
    <output id="output"></output>
</section>
<hr>
<!-- Button to clear the localStorage for this Domain -->
<section>
    <button type="button" id="clear">Clear localStorage</button>
</section>
|LiveURL=http://jsfiddle.net/DM6hB/6/
}}{{Single Example
|Language=JavaScript
|Description=Functions and event handlers for saving, reading and clearing localStorage items.
|Code=
/* global document, window */
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
}}
}}
{{Notes_Section
|Usage=Use via the methods ''setItem'', ''getItem'', ''removeItem'' and ''clear'' provided by [[apis/web-storage/Storage]].

Listen to the storage event on [[dom/Window]] to catch changes in the storage (example: http://jsfiddle.net/A6tuM/1/).
|Notes=The '''localStorage''' "property" provides an instance of a  storage area object, to which the '''Storage''' object's properties and methods are applied.
|Import_Notes=The amount of storage is limited by the browser on a per location basis (e.g. per domain). An error message is thrown, when the quota is exceed. 

See for an example of the error message here (the example shows the error message for when the [[apis/web-storage/Storage/sessionStorage|sessionStorage]] quota is exceeded. The behavior is similar for localStorage): http://jsfiddle.net/wkDc6/1/
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Storage Specification
|URL=http://www.w3.org/TR/webstorage/
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=Off-line Storage
}}
{{Topics|Webstorage}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}