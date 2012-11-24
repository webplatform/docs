{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Non standard. Proprietary. Retrieves the information from the clipboard as part of clipboard operation events.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the [[dom/methods/setData|'''setData''']] and [[dom/methods/getData|'''getData''']] methods with the '''clipboardData''' object to perform a cut-and-paste operation through the shortcut menu.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;style&gt;
BODY {
 margin-top: 0;
 margin-left: 0;
 background: #ffffff;
}
A, A:link, A:active {
 color: #000000;
}
A:visited {
 color: #808080;
}
  &lt;/style&gt;
  &lt;script&gt;
var bResult, oSource;
// Select the text to be cut. Trailing spaces in a text
// selection in cut events cause the Cut shortcut menu item to
// remain disabled.
function fnLoad() {
    var r {{=}} document.body.createTextRange();
    oSource = document.getElementById("oSource");
    r.findText(oSource.textContent);
    r.select();
}
// Enable the Cut shortcut menu item over the DIV. Cut is disabled by default.
// Once Cut is enabled, Internet Explorer automatically copies the data to the
// clipboard and removes the selected text from the document.
function fnBeforeCut(event) {
	event.preventDefault();
}
//Assign data in text format to the window.clipboardData object.
//Display the result (Boolean) from the setData method in the input box below.
function fnCut(event){
	event.preventDefault();
	bResult {{=}} window.clipboardData.setData("Text", oSource.textContent);
	oSource.textContent{{=}} "";
	document.getElementById("tText").textContent +{{=}} bResult;
}
// Enable the Paste shortcut menu item over the DIV. Paste is disabled by default.
function fnBeforePaste(event) {
	event.preventDefault();
}
// Prevent the default action in onpaste for the text input, which
// has a default behavior.
function fnPaste(event) {
	event.preventDefault();
	document.getElementById("oTarget").textContent {{=}} window.clipboardData.getData("Text");
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body onload{{=}}"fnLoad()"&gt;
  &lt;div class{{=}}"clsSource" id{{=}}"oSource"
          onbeforecut{{=}}"fnBeforeCut(event)" oncut{{=}}"fnCut(event)"&gt;
	Select and cut this text
  &lt;/div&gt;
  &lt;div class{{=}}"clsTarget" id{{=}}"oTarget"
          onbeforepaste{{=}}"fnBeforePaste(event)" onpaste{{=}}"fnPaste(event)"&gt;
	Paste the Text Here
  &lt;/div&gt;&lt;br/&gt;
  &lt;span class{{=}}"clsData"&gt;setData Result: &lt;/span&gt;
  &lt;input class{{=}}"clsText" id{{=}}"tText" type{{=}}"text"
            readonly="readonly" value{{=}}"" size{{=}}"6"
            tabindex{{=}}"-1"&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipboardDataEX.htm
}}
}}
{{Notes_Section
|Notes=The '''clipboardData''' object is reserved for copy/cut/paste operations. It transfers information using the system clipboard, and retains it until data from the next editing operation replaces it. This form of data transfer is particularly suited to multiple pastes of the same data.
|Import_Notes====Additional Members (MSDN)===
The '''clipboardData''' object has these types of members:
[[#Additional_Methods|Additional Methods]]


====Additional Methods====
The '''clipboardData''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/clearData|'''clearData''']]
{{!}}Removes one or more data formats from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
{{!}}-
{{!}}[[dom/methods/getData|'''getData''']]
{{!}}Gets the data in the specified format from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
{{!}}-
{{!}}[[dom/methods/setData|'''setData''']]
{{!}}Assigns data in a specified format to the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications=
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
|Internet_explorer_supported=Yes
|Internet_explorer_version=5
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
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}