{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the [[dom/methods/setData|'''setData''']] and [[dom/methods/getData|'''getData''']] methods with the '''clipboardData''' object to perform a cut-and-paste operation through the shortcut menu.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipboardDataEX.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var bResult;
// Select the text to be cut. Trailing spaces in a text
// selection in cut events cause the Cut shortcut menu item to
// remain disabled.
function fnLoad() {
    var r {{=}} document.body.createTextRange();
    r.findText(oSource.innerText);
    r.select();
}
// Enable the Cut shortcut menu item over the DIV. Cut is disabled by default.
// Once Cut is enabled, Internet Explorer automatically copies the data to the
// clipboard and removes the selected text from the document.
function fnBeforeCut() {
    event.returnValue {{=}} false;
}
//Assign data in text format to the window.clipboardData object.
//Display the result (Boolean) from the setData method in the input box below.
function fnCut(){
	event.returnValue {{=}} false;
	bResult {{=}} window.clipboardData.setData("Text",oSource.innerText);
	oSource.innerText {{=}} "";
	tText.innerText +{{=}} bResult;
}
// Enable the Paste shortcut menu item over the DIV. Paste is disabled by default.
function fnBeforePaste() {
    event.returnValue {{=}} false;
}
// Cancel the returnValue in onpaste for the text input, which
// has a default behavior.
function fnPaste() {
    event.returnValue {{=}} false;
	oTarget.innerText {{=}} window.clipboardData.getData("Text");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"fnLoad()" TOPMARGIN{{=}}0 LEFTMARGIN{{=}}0 BGPROPERTIES{{=}}"fixed" BGCOLOR{{=}}"#FFFFFF"
	LINK{{=}}"#000000" VLINK{{=}}"#808080" ALINK{{=}}"#000000"&gt;
&lt;DIV CLASS{{=}}"clsSource" ID{{=}}"oSource" onbeforecut{{=}}"fnBeforeCut()" oncut{{=}}"fnCut()"&gt;
	Select and cut this text
&lt;/DIV&gt;
&lt;DIV CLASS{{=}}"clsTarget" ID{{=}}"oTarget" onbeforepaste{{=}}"fnBeforePaste()" onpaste{{=}}"fnPaste()"&gt;
	Paste the Text Here
&lt;/DIV&gt;&lt;BR&gt;
&lt;SPAN CLASS{{=}}"clsData"&gt;setData Result: &lt;/SPAN&gt;
&lt;INPUT CLASS{{=}}"clsText" ID{{=}}"tText" TYPE{{=}}"text" READONLY VALUE{{=}}"" SIZE{{=}}"6" TABINDEX{{=}}"-1"&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''clipboardData''' object is reserved for editing actions performed through the '''Edit''' menu, shortcut menus, and shortcut keys. It transfers information using the system clipboard, and retains it until data from the next editing operation replaces it. This form of data transfer is particularly suited to multiple pastes of the same data.
This object is available in script as of Microsoft Internet Explorer 5.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''clipboardData''' object has these types of members:
*[#methods Methods]


====Methods====
The '''clipboardData''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/clearData|'''clearData''']]
|Removes one or more data formats from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
|-
|[[dom/methods/getData|'''getData''']]
|Gets the data in the specified format from the clipboard through the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
|-
|[[dom/methods/setData|'''setData''']]
|Assigns data in a specified format to the [[dom/objects/dataTransfer|'''dataTransfer''']] object or the '''clipboardData''' object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Data Transfer Overview</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}