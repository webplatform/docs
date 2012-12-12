{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example lets the user choose one or more files, and then displays the choices.  The files list can also be used to upload to a website.

<span codelanguage{{=}}"HTML"><table>
<tr>
<th>HTML</th>
</tr>
<tr>
<td>
<pre>&lt;!DOCTYPE html&gt;
&lt;html &gt;
&lt;head&gt;
&lt;title&gt;Files property test&lt;/title&gt; 
&lt;script type{{=}}"text/javascript"&gt;
function getFiles() {
// Get input element
myFileList {{=}} document.getElementById("myfiles");
// loop through files property, using length to get number of files chosen
for (var i {{=}} 0; i &lt; myFileList.files.length; i++) {
// display them in the div
document.getElementById("display").innerHTML +{{=}} "&lt;br/&gt;" + myFileList.files[i].name ;
}
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;label&gt;Use &lt;strong&gt;shift&lt;/strong&gt; or &lt;strong&gt;ctrl&lt;/strong&gt; click to pick a few files: 
&lt;input type{{=}}"file" multiple id{{=}}"myfiles" onchange{{=}}"getFiles();" /&gt;&lt;/label&gt;

&lt;div id{{=}}"display"&gt;&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
</td>
</tr>
</table></span>

The following examples use the '''INPUT type{{=}}file''' element to upload a file to a server. The first example requires Microsoft Posting Acceptor, which can be used with IIS or Personal Web Server.
|Code=&lt;form name{{=}}"oForm"
   action{{=}}"repost.asp"
   enctype{{=}}"multipart/form-data"
   method{{=}}"post"&gt;
&lt;input type{{=}}"file" name{{=}}"oFile1"/&gt;
&lt;input type{{=}}"submit" value{{=}}"Upload File"&gt;
&lt;/form&gt;
|LiveURL=This example uses HTML code to submit a file selected by the user to Cpshost.dll, which is installed with Posting Acceptor.
}}{{Single Example
|Description=This example shows the Active Server Page (ASP) content of Repost.asp. Notice that the properties of the uploaded file are accessible from the submitted form.
|Code=&lt;%@ LANGUAGE {{=}} JScript %&gt;
&lt;%
   Response.buffer{{=}}true;
%&gt;
&lt;html&gt;
&lt;title&gt;Repost Example&lt;/title&gt;
&lt;body&gt;
&lt;h1&gt;Upload Status&lt;/h1&gt;
&lt;p&gt; 
Destination: &lt;b&gt;&lt;% Response.Write(Server.HTMLEncode(Request.Form("TargetURL"))) %&gt;&lt;/b&gt; 
&lt;/p&gt; 
&lt;% 
   Response.write("&lt;P&gt;Name: " + Server.HTMLEncode(Request.Form("FileName")) + "&lt;/P&gt;"); 
   Response.write("&lt;P&gt;Size: " + Server.HTMLEncode(Request.Form("FileSize")) + "&lt;/P&gt;"); 
   Response.write("&lt;P&gt;Path: " + Server.HTMLEncode(Request.Form("FilePath")) + "&lt;/P&gt;"); 
%&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
For a file upload to take place:
*The '''INPUT type{{=}}file''' element must be enclosed within a '''FORM''' element.
*A value must be specified for the [[html/attributes/name|'''NAME''']] attribute of the '''INPUT type{{=}}file''' element.
*The [[html/attributes/method|'''METHOD''']] attribute of the '''FORM''' element must be set to '''post'''.
*The [[html/attributes/encoding|'''ENCTYPE''']] attribute of the '''FORM''' element must be set to multipart/form-data.

'''Note'''  For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
To handle a file upload to the server, a server-side process must be running that can handle multipart/form-data submissions. For example, the Microsoft Posting Acceptor allows Microsoft Internet Information Server (IIS) to accept file uploads. Additional Common Gateway Interface (CGI) scripts that can handle multipart/form-data submissions are available on the Web.

Windows Internet Explorer 8 and later. When a file is selected by using the '''input type{{=}}file''' object, the value of the [[dom/properties/value (type/file) B685|'''value''']] property depends on the value of the "Include local directory path when uploading files to a server" security setting for the security zone used to display the Web page containing the '''input''' object. For more information, see [[dom/properties/value (type/file) B685|'''value''']].
Windows Internet Explorer 7 and later.  By default, Internet Explorer does not include folder or directory path information when uploading files to sites in the Restricted zone.  This improves security by preventing information disclosure. Also, to improve accessibility, the '''INPUT type{{=}}file''' element now contains two accessible elements—one for the input box and one for the '''Browse''' button. This change is applicable only to accessibility tools; script implementations are not affected.
Microsoft Internet Explorer 6 for Windows XP Service Pack 2 (SP2) and later.  For security reasons, the '''input type{{=}}file''' element no longer accepts relative file paths.  Microsoft Internet Explorer raises an Access Denied exception when the user attempts to submit a form containing an '''input type{{=}}file''' element that contains a relative path.
The '''INPUT type{{=}}file''' element is available in HTML and script as of Microsoft Internet Explorer 4.0. The file upload add-on is required to use the '''INPUT type{{=}}file''' element in Microsoft Internet Explorer 3.02. Users can enter a file path in the text box or click the '''Browse''' button to browse the file system. When a file is uploaded, the file name is also submitted.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10


===HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}forbidden
{{!}}-
!CSS Display
{{!}}inline
{{!}}}

===Members===
The '''input type{{=}}file''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''input type{{=}}file''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/activate|'''onactivate''']]
|Fires when the object is set as the [[dom/properties/activeElement|'''active element''']].
|-
|[[dom/events/afterupdate|'''onafterupdate''']]
|Fires on a databound object after successfully updating the associated data in the data source object.
|-
|[[dom/events/beforeactivate|'''onbeforeactivate''']]
|Fires immediately before the object is set as the [[dom/properties/activeElement|'''active element''']].
|-
|[[dom/events/beforecopy|'''onbeforecopy''']]
|Fires on the source object before the selection is copied to the system clipboard.
|-
|[[dom/events/beforecut|'''onbeforecut''']]
|Fires on the source object before the selection is deleted from the document.
|-
|[[dom/events/beforedeactivate|'''onbeforedeactivate''']]
|Fires immediately before the [[dom/properties/activeElement|'''activeElement''']] is changed from the current object to another object in the parent document.
|-
|[[dom/events/beforeeditfocus|'''onbeforeeditfocus''']]
|Fires before an object contained in an editable element enters a ''UI Activation'' state or when an editable container object is ''control selection''.
|-
|[[dom/events/beforepaste|'''onbeforepaste''']]
|Fires on the target object before the selection is pasted from the system clipboard to the document.
|-
|[[dom/events/beforeupdate|'''onbeforeupdate''']]
|Fires on a databound object before updating the associated data in the data source object.
|-
|[[dom/events/blur|'''onblur''']]
|Fires when the object loses the input focus.
|-
|[[dom/events/cellchange|'''oncellchange''']]
|Fires when data changes in the data provider.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/click|'''onclick''']]
|Fires when the user clicks the left mouse button on the object.
|-
|[[dom/events/contextmenu|'''oncontextmenu''']]
|Fires when the user clicks the right mouse button in the client area, opening the context menu.
|-
|[[dom/events/controlselect|'''oncontrolselect''']]
|Fires when the user is about to make a ''control selection'' of the object.
|-
|[[dom/events/cut|'''oncut''']]
|Fires on the source element when the object or selection is removed from the document and added to the system clipboard.
|-
|[[dom/events/dataavailable|'''ondataavailable''']]
|Fires periodically as data arrives from data source objects that asynchronously transmit their data.
|-
|[[dom/events/datasetchanged|'''ondatasetchanged''']]
|Fires when the data set exposed by a data source object changes.
|-
|[[dom/events/datasetcomplete|'''ondatasetcomplete''']]
|Fires to indicate that all data is available from the data source object.
|-
|[[dom/events/dblclick|'''ondblclick''']]
|Fires when the user double-clicks the object.
|-
|[[dom/events/deactivate|'''ondeactivate''']]
|Fires when the [[dom/properties/activeElement|'''activeElement''']] is changed from the current object to another object in the parent document.
|-
|[[dom/events/drag|'''ondrag''']]
|Fires on the source object continuously during a drag operation.
|-
|[[dom/events/dragend|'''ondragend''']]
|Fires on the source object when the user releases the mouse at the close of a drag operation.
|-
|[[dom/events/dragenter|'''ondragenter''']]
|Fires on the target element when the user drags the object to a valid drop target.
|-
|[[dom/events/dragleave|'''ondragleave''']]
|Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
|-
|[[dom/events/dragover|'''ondragover''']]
|Fires on the target element continuously while the user drags the object over a valid drop target.
|-
|[[dom/events/dragstart|'''ondragstart''']]
|Fires on the source object when the user starts to drag a text selection or selected object.
|-
|[[dom/events/drop|'''ondrop''']]
|Fires on the target object when the mouse button is released during a drag-and-drop operation.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/errorupdate|'''onerrorupdate''']]
|Fires on a databound object when an error occurs while updating the associated data in the data source object.
|-
|[[dom/events/filterchange|'''onfilterchange''']]
|Fires when a visual filter changes state or completes a transition.
|-
|[[dom/events/focus|'''onfocus''']]
|Fires when the object receives focus.
|-
|[[dom/events/focusin|'''onfocusin''']]
|Fires for an element just prior to setting focus on that element.
|-
|[[dom/events/focusout|'''onfocusout''']]
|Fires for the current element with focus immediately after moving focus to another element.
|-
|[[dom/events/help|'''onhelp''']]
|Fires when the user presses the F1 key while the client is the active window.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/keydown|'''onkeydown''']]
|Fires when the user presses a key.
|-
|[[dom/events/keypress|'''onkeypress''']]
|Fires when the user presses an alphanumeric key.
|-
|[[dom/events/keyup|'''onkeyup''']]
|Fires when the user releases a key.
|-
|[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
|Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[dom/events/losecapture|'''onlosecapture''']]
|Fires when the object loses the mouse capture.
|-
|[[dom/events/mousedown|'''onmousedown''']]
|Fires when the user clicks the object with either mouse button.
|-
|[[dom/events/mouseenter|'''onmouseenter''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseleave|'''onmouseleave''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mousemove|'''onmousemove''']]
|Fires when the user moves the mouse over the object.
|-
|[[dom/events/mouseout|'''onmouseout''']]
|Fires when the user moves the mouse pointer outside the boundaries of the object.
|-
|[[dom/events/mouseover|'''onmouseover''']]
|Fires when the user moves the mouse pointer into the object.
|-
|[[dom/events/mouseup|'''onmouseup''']]
|Fires when the user releases a mouse button while the mouse is over the object.
|-
|[[dom/events/mousewheel|'''onmousewheel''']]
|Fires when the wheel button is rotated.
|-
|[[dom/events/move|'''onmove''']]
|Fires when the object moves.
|-
|[[dom/events/moveend|'''onmoveend''']]
|Fires when the object stops moving.
|-
|[[dom/events/movestart|'''onmovestart''']]
|Fires when the object starts to move.
|-
|[[dom/events/paste|'''onpaste''']]
|Fires on the target object when the user pastes data, transferring the data from the system clipboard to the document.
|-
|[[dom/events/propertychange|'''onpropertychange''']]
|Fires when a property changes on the object.
|-
|[[dom/events/readystatechange|'''onreadystatechange''']]
|Fires when the state of the object has changed.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[dom/events/resize|'''onresize''']]
|Fires when the size of the object is about to change.
|-
|[[dom/events/resizeend|'''onresizeend''']]
|Fires when the user finishes changing the dimensions of the object in a ''control selection''.
|-
|[[dom/events/resizestart|'''onresizestart''']]
|Fires when the user begins to change the dimensions of the object in a ''control selection''.
|-
|[[dom/events/rowenter|'''onrowenter''']]
|Fires to indicate that the current row has changed in the data source and new data values are available on the object.
|-
|[[dom/events/rowexit|'''onrowexit''']]
|Fires just before the data source control changes the current row in the object.
|-
|[[dom/events/rowsdelete|'''onrowsdelete''']]
|Fires when rows are about to be deleted from the recordset.
|-
|[[dom/events/rowsinserted|'''onrowsinserted''']]
|Fires just after new rows are inserted in the current recordset.
|-
|[[dom/events/scroll|'''onscroll''']]
|Fires when the user repositions the scroll box in the scroll bar on the object.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|-
|[[dom/events/select|'''onselectstart''']]
|Fires when the object is being selected.
|}
 

====Methods====
The '''input type{{=}}file''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''addBehavior'''
|Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
|-
|[[dom/methods/appendChild|'''appendChild''']]
|Appends an element as a child to the object.
|-
|[[dom/methods/applyElement|'''applyElement''']]
|Makes the element either a child or parent of another element.
|-
|[[dom/methods/attachEvent|'''attachEvent''']]
|Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
|-
|[[dom/methods/blur|'''blur''']]
|Causes the element to lose focus and fires the [[dom/events/blur|'''onblur''']] event.
|-
|[[dom/methods/clearAttributes|'''clearAttributes''']]
|Removes all attributes and values from the object.
|-
|[[dom/methods/click|'''click''']]
|Simulates a click by causing the [[dom/events/click|'''onclick''']] event to fire.
|-
|[[dom/methods/cloneNode|'''cloneNode''']]
|Copies a reference to the object from the document hierarchy.
|-
|[[dom/methods/compareDocumentPosition|'''compareDocumentPosition''']]
|Compares the position of two nodes in a document.
|-
|[[dom/methods/componentFromPoint|'''componentFromPoint''']]
|Returns the component located at the specified coordinates via certain events.
|-
|'''contains'''
|Checks whether the given element is contained within the object.
|-
|[[dom/methods/detachEvent|'''detachEvent''']]
|Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
|-
|[[dom/methods/doScroll|'''doScroll''']]
|Simulates a click on a scroll bar component.
|-
|[[dom/methods/dragDrop|'''dragDrop''']]
|Initiates a drag event.
|-
|[[dom/methods/fireEvent|'''fireEvent''']]
|Fires a specified event on the object.
|-
|[[dom/methods/focus|'''focus''']]
|Causes the element to receive the focus and executes the code specified by the [[dom/events/focus|'''onfocus''']] event.
|-
|[[dom/methods/getAdjacentText|'''getAdjacentText''']]
|Returns the adjacent text string.
|-
|[[dom/methods/getAttribute|'''getAttribute''']]
|Retrieves the value of the specified attribute.
|-
|[[dom/methods/getAttributeNode|'''getAttributeNode''']]
|Retrieves an [[dom/attributes|'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name|'''name''']] property.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']]
|Retrieves an object that specifies the bounds of a collection of [[dom/TextRectangle|'''TextRectangle''']] objects.
|-
|[[dom/methods/getClientRects|'''getClientRects''']]
|Retrieves a collection of rectangles that describes the layout of the contents of an object or range within the client. Each rectangle describes a single line.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttribute|'''hasAttribute''']]
|Determines whether an attribute with the specified name exists.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/hasAttributes|'''hasAttributes''']]
|Determines whether one or more attributes exist for the object.
|-
|[[dom/methods/hasChildNodes|'''hasChildNodes''']]
|Returns a value that indicates whether the object has children.
|-
|[[dom/methods/insertAdjacentElement|'''insertAdjacentElement''']]
|Inserts an element at the specified location.
|-
|[[dom/methods/insertAdjacentHTML|'''insertAdjacentHTML''']]
|Inserts the given HTML text into the element at the location.
|-
|[[dom/methods/insertAdjacentText|'''insertAdjacentText''']]
|Inserts the given text into the element at the specified location.
|-
|[[dom/methods/insertBefore|'''insertBefore''']]
|Inserts an element into the document hierarchy as a child node of a parent object.
|-
|[[dom/methods/isDefaultNamespace|'''isDefaultNamespace''']]
|Indicates whether or not a namespace is the default namespace for a document.
|-
|[[dom/methods/isEqualNode|'''isEqualNode''']]
|Determines if two nodes are equal.
|-
|[[dom/methods/isSameNode|'''isSameNode''']]
|Determines if two node references refer to the same node.
|-
|[[dom/methods/isSupported|'''isSupported''']]
|Returns a value indicating whether or not the object supports a specific DOM standard.
|-
|[[dom/methods/lookupNamespaceURI|'''lookupNamespaceURI''']]
|Gets the URI of the namespace associated with a namespace prefix, if any.
|-
|[[dom/methods/lookupPrefix|'''lookupPrefix''']]
|Gets the namespace prefix associated with a URI, if any.
|-
|[[dom/methods/mergeAttributes|'''mergeAttributes''']]
|Copies all read/write attributes to the specified element.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/normalize|'''normalize''']]
|Merges adjacent DOM objects to produce a normalized document object model.
|-
|[[css/selectors api/querySelector|'''querySelector''']]
|Retrieves the first DOM 
element node from descendants of the starting element node
that match any selector within the supplied selector string.
|-
|[[css/selectors api/querySelectorAll|'''querySelectorAll''']]
|Retrieves all DOM 
element nodes from descendants of the starting element node 
that match any selector within the supplied selector strings.
|-
|[[dom/methods/releaseCapture|'''releaseCapture''']]
|Removes mouse capture from the object in the current document.
|-
|[[dom/methods/removeAttribute|'''removeAttribute''']]
|Removes an attribute from an object.
|-
|[[dom/methods/removeAttributeNode|'''removeAttributeNode''']]
|Removes an [[dom/attributes|'''attribute''']] object from the object.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|'''removeBehavior'''
|Detaches a behavior from the element.
|-
|[[dom/methods/removeChild|'''removeChild''']]
|Removes a child node from the object.
|-
|[[dom/methods/removeNode|'''removeNode''']]
|Removes the object from the document hierarchy.
|-
|[[dom/methods/replaceAdjacentText|'''replaceAdjacentText''']]
|Replaces the text adjacent to the element.
|-
|[[dom/methods/replaceChild|'''replaceChild''']]
|Replaces an existing child element with a new child element.
|-
|[[dom/methods/replaceNode|'''replaceNode''']]
|Replaces the object with another element.
|-
|[[dom/traversal/methods/scrollIntoView|'''scrollIntoView''']]
|Causes the object to scroll into view, aligning it either at the top or bottom of the window.
|-
|[[dom/methods/select|'''select''']]
|Highlights the input area of a form element.
|-
|[[dom/methods/setActive|'''setActive''']]
|Sets the object as active without setting focus to the object.
|-
|[[dom/methods/setAttribute|'''setAttribute''']]
|Sets the value of the specified attribute.
|-
|[[dom/methods/setAttributeNode|'''setAttributeNode''']]
|Sets an [[dom/attributes|'''attribute''']] object node as part of the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/setCapture|'''setCapture''']]
|Sets the mouse capture to the object that belongs to the current document.
|-
|[[dom/methods/swapNode|'''swapNode''']]
|Exchanges the location of two objects in the document hierarchy.
|}
 

====Properties====
The '''input type{{=}}file''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/accessKey|'''accessKey''']]
|Sets or retrieves the access key for the object.
|-
|[[html/attributes/ATOMICSELECTION html_attribute|'''ATOMICSELECTION''']]
|Specifies whether the element and its contents must be selected as a whole, indivisible unit.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[dom/properties/canHaveChildren|'''canHaveChildren''']]
|Gets a value indicating whether the object can contain child objects.
|-
|[[dom/properties/canHavedom/canHaveHTML|'''canHaveHTML''']]
|Retrieves the value indicating whether the object can contain rich HTML markup.
|-
|[[dom/traversal/properties/childElementCount|'''childElementCount''']]
|Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. [[dom/traversal/properties/childElementCount|'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType|'''nodeType''']] {{=}}1, or element nodes.
|-
|[[dom/properties/className|'''className''']]
|Sets or retrieves the class of the object.
|-
|[[dom/properties/clientHeight|'''clientHeight''']]
|Retrieves the height of the object including padding, but not including margin, border, or scroll bar.
|-
|[[dom/properties/clientLeft|'''clientLeft''']]
|Retrieves the distance between the [[dom/properties/offsetLeft|'''offsetLeft''']] property and the true left side of the client area.
|-
|[[dom/properties/clientTop|'''clientTop''']]
|Retrieves the distance between the [[dom/properties/offsetTop|'''offsetTop''']] property and the true top of the client area.
|-
|[[dom/properties/clientWidth|'''clientWidth''']]
|Retrieves the width of the object including padding, but not including margin, border, or scroll bar.
|-
|[[dom/properties/defaultValue|'''defaultValue''']]
|Sets or retrieves the initial contents of the object.
|-
|[[html/attributes/dir|'''dir''']]
|Sets or retrieves the reading order of the object.
|-
|[[html/attributes/disabled|'''disabled''']]
|Sets or retrieves a value that indicates whether the user can interact with the object.
|-
|[[dom/properties/files|'''files''']]
|Returns a [[apis/file/FileList|'''FileList''']] object on a '''file type input''' object.
|-
|[[dom/properties/firstChild|'''firstChild''']]
|Gets a reference to the first child in the [[dom/properties/childNodes|'''childNodes''']] collection of the object.
|-
|[[dom/traversal/properties/firstElementChild|'''firstElementChild''']]
|Retrieves a reference to the first child element, or NULL if there are no child elements.
|-
|[[dom/properties/form|'''form''']]
|Retrieves a reference to the form that the object is embedded in.
|-
|[[html/attributes/hideFocus|'''hideFocus''']]
|Sets or gets the value that indicates whether the object visibly shows that it has focus.
|-
|[[html/attributes/id|'''id''']]
|Sets or retrieves the string identifying the object.
|-
|[[dom/properties/innerdom/innerHTML|'''innerHTML''']]
|Sets or retrieves the HTML between the start and end tags of the object.
|-
|[[dom/properties/innerText|'''innerText''']]
|Sets or retrieves the text between the start and end tags of the object.
|-
|[[dom/properties/isContentEditable|'''isContentEditable''']]
|Gets the value that indicates whether the user can edit the contents of the object.
|-
|[[dom/properties/isDisabled|'''isDisabled''']]
|Gets the value that indicates whether the user can interact with the object.
|-
|[[dom/properties/isMultiLine|'''isMultiLine''']]
|Retrieves the value indicating whether the content of the object contains one or more lines.
|-
|[[dom/traversal/properties/isTextEdit|'''isTextEdit''']]
|Retrieves whether a [[dom/traversal/TextRange|'''TextRange''']] object can be created using the object.
|-
|[[html/attributes/lang|'''lang''']]
|Sets or retrieves the language to use.
|-
|[[html/attributes/language|'''language''']]
|Sets or retrieves the language in which the current script is written.
|-
|[[dom/properties/lastChild|'''lastChild''']]
|Gets a reference to the last child in the [[dom/properties/childNodes|'''childNodes''']] collection of an object.
|-
|[[dom/traversal/properties/lastElementChild|'''lastElementChild''']]
|Retrieves a reference to the last child element or NULL if there are no child elements.
|-
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[html/attributes/name|'''name''']]
|Sets or retrieves the name of the object.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
|-
|[[dom/traversal/properties/nextElementSibling|'''nextElementSibling''']]
|Retrieves a reference to the sibling element that immediately follows or NULL if the element does not have any sibling elements that follow it.
|-
|[[dom/properties/nextSibling|'''nextSibling''']]
|Retrieves a reference to the next child of the parent for the object.
|-
|[[dom/properties/nodeName|'''nodeName''']]
|Gets the name of a particular type of node.
|-
|[[dom/properties/nodeType|'''nodeType''']]
|Retrieves the type of the requested node.
|-
|[[dom/properties/nodeValue|'''nodeValue''']]
|Gets or sets the value of a node.
|-
|[[dom/properties/offsetHeight|'''offsetHeight''']]
|Retrieves the height of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetLeft|'''offsetLeft''']]
|Retrieves the calculated left position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetParent|'''offsetParent''']]
|Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|'''offsetTop''']] and [[dom/properties/offsetLeft|'''offsetLeft''']] properties of the object.
|-
|[[dom/properties/offsetTop|'''offsetTop''']]
|Retrieves the calculated top position of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/offsetWidth|'''offsetWidth''']]
|Retrieves the width of the object relative to the layout or coordinate parent, as specified by the [[dom/properties/offsetParent|'''offsetParent''']] property.
|-
|[[dom/properties/outerdom/outerHTML|'''outerHTML''']]
|Sets or retrieves the object and its content in HTML.
|-
|[[dom/properties/outerText|'''outerText''']]
|Sets or retrieves the text of the object.
|-
|[[dom/properties/ownerDocument|'''ownerDocument''']]
|Retrieves the [[dom/document|'''document''']] object associated with the node.
|-
|[[dom/traversal/properties/parentElement|'''parentElement''']]
|Retrieves the parent object in the object hierarchy.
|-
|[[dom/properties/parentNode|'''parentNode''']]
|Retrieves the parent object in the document hierarchy.
|-
|[[dom/traversal/properties/parentTextEdit|'''parentTextEdit''']]
|Retrieves the container object in the document hierarchy that can be used to create a [[dom/traversal/TextRange|'''TextRange''']] containing the original object.
|-
|[[dom/properties/prefix|'''prefix''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[dom/traversal/properties/previousElementSibling|'''previousElementSibling''']]
|Retrieves a reference to the immediately preceding sibling element or NULL if the element does not have any preceding siblings.
|-
|[[dom/properties/previousSibling|'''previousSibling''']]
|Gets a reference to the previous child of the parent for the object.
|-
|[[dom/properties/readyState (Link, Img, Input, Style...elements)|'''readyState''']]
|Retrieves a value that indicates the current state of the object.
|-
|'''recordNumber'''
|Retrieves the ordinal record from the data set that generated the object.
|-
|[[html/attributes/role|'''role''']]
|Sets or retrieves the role for this element.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/scrollHeight|'''scrollHeight''']]
|Retrieves the scrolling height of the object.
|-
|[[dom/properties/scrollLeft|'''scrollLeft''']]
|Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollTop|'''scrollTop''']]
|Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollWidth|'''scrollWidth''']]
|Retrieves the scrolling width of the object.
|-
|[[html/attributes/size (control)|'''size''']]
|Sets or retrieves the size of the control.
|-
|[[dom/properties/sourceIndex|'''sourceIndex''']]
|Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|'''all''']] collection.
|-
|[[html/attributes/STYLE html_attribute|'''STYLE''']]
|Sets an inline style for the element.
|-
|[[html/attributes/tabIndex|'''tabIndex''']]
|Sets or retrieves the index that defines the tab order for the object.
|-
|[[dom/properties/tagName|'''tagName''']]
|Retrieves the tag name of the object.
|-
|[[dom/properties/tagUrn|'''tagUrn''']]
|Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/textContent|'''textContent''']]
|Sets or retrieves the text content of an object and any child objects.
|-
|[[html/attributes/title|'''title''']]
|Sets or retrieves advisory information (a ToolTip) for the object.
|-
|[[html/attributes/type|'''type''']]
|Retrieves or initially sets  the type of '''input''' control represented by the object.
|-
|[[dom/properties/uniqueID|'''uniqueID''']]
|Retrieves an autogenerated, unique identifier for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|-
|[[dom/properties/value (type/file) B685|'''value''']]
|Retrieves the file name of the '''input''' object after the text is set by user input.
|-
|[[html/attributes/value (input elements)|'''value''']]
|Sets or retrieves the displayed value for the control object.  This value is returned to the server when the control object is submitted.
|-
|[[html/attributes/width  (img, input elements)|'''width''']]
|Sets or retrieves the calculated width of the object.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.02
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=1.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
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
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>input</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}