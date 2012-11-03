{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=dom/HTMLIFrameElement
|Content=Iframes are one the best ways to build a complex, detailed webpage from smaller, more manageable chunks.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''iframe''' element and an HTML fragment to create a frame containing the page sample.htm.
|Code=&lt;IFRAME ID{{=}}IFrame1 FRAMEBORDER{{=}}0 SCROLLING{{=}}NO SRC{{=}}"sample.htm"&gt;&lt;/IFRAME&gt;
}}{{Single Example
|Description=This example returns a reference to the [[dom/properties/all|'''all''']] collection of the document contained by the '''iframe'''.
|Code=var collAll {{=}} document.frames("IFrame1").document.all
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''iframe''' element functions as a document within a document, or like a floating '''frame'''. The [[dom/properties/frames|'''frames''']] collection provides access to the contents of an '''iframe'''. Use the '''frames''' collection to read or write to elements contained in an '''iframe'''. For example, the syntax for accessing the [[css/properties/background-color|'''backgroundColor''']] style of the '''body''' object in an '''iframe''' is:
 <code>sColor {{=}} document.frames("sFrameName").document.body.style.backgroundColor;</code>
You can access the '''iframe''' object's properties, but not its contents, through the object model of the page where the '''iframe''' object resides. For example, the syntax for accessing the [[css/properties/border|'''border''']] style of the '''iframe''' object is:
 <code>sBorderValue {{=}} document.all.oFrame.style.border;</code>
'''Note'''  Properties of the '''iframe''' must be accessed using the prefix, <code>document.all</code>, for example, <code>document.all.iframeId.marginWidth</code>.

'''Security Warning:  '''
To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. To treat the content of the '''iframe''' as if it were in the Restricted Sites zone, set the '''SECURITY''' attribute to "restricted." For more information about using the Dynamic HTML (DHTML) object model with the '''frame''' and '''iframe''' objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML.
Windows Internet Explorer 8 and later. The values of the [[html/attributes/longDesc|'''longDesc''']] and [[html/attributes/src (iframe, embed, xml)|'''src''']] attributes depend on the current document compatibility mode.
Windows Internet Explorer 7 and later. For security reasons, resizing is disabled for '''iframe''' objects that display content hosted on a domain different from the domain hosting the parent document. If you trust the content you are loading into an '''iframe''' object, you can enable resizing by specifying values for the [[css/properties/min-width|'''minWidth''']] and [[css/properties/max-width|'''maxWidth''']] attributes of the '''iframe''' element in the source of the parent document. You must specify values for both attributes to enable resizing.
Microsoft Internet Explorer 5.5 supports transparent content with inline floating frames. The following conditions must be met to define transparent content for inline floating frames.
#The [[html/attributes/allowTransparency|'''allowTransparency''']] attribute, used with the '''iframe''' element, must be set to <code>true</code>.
#In the '''iframe''' content source document, the  [[css/properties/background-color|'''backgroundColor''']] attribute of the '''body''' element must be set to <code>transparent</code>.

Using Transparency with Inline Floating Frames
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 16.5


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|block
|}

===Members===
The '''iframe''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''iframe''' object has these events.
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
|[[dom/events/beforecopy|'''onbeforecopy''']]
|Fires on the source object before the selection is copied to the system clipboard.
|-
|[[dom/events/beforedeactivate|'''onbeforedeactivate''']]
|Fires immediately before the [[dom/properties/activeElement|'''activeElement''']] is changed from the current object to another object in the parent document.
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
|[[dom/events/controlselect|'''oncontrolselect''']]
|Fires when the user is about to make a ''control selection'' of the object.
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
|[[dom/events/deactivate|'''ondeactivate''']]
|Fires when the [[dom/properties/activeElement|'''activeElement''']] is changed from the current object to another object in the parent document.
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
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
|Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
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
|}
 

====Methods====
The '''iframe''' object has these methods.
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
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagName|'''getElementsByTagName''']]
|Retrieves a collection of objects based on the specified element name.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[svg/methods/getSVGDocument|'''getSVGDocument''']]
|Gets Document object for the referenced document, or null if there is no document.
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
The '''iframe''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/align (Table, iframe elements)|'''align''']]
|Sets or retrieves a value that indicates the table alignment.
|-
|[[html/attributes/allowTransparency|'''allowTransparency''']]
|Sets or retrieves whether the object can be transparent.
|-
|[[html/attributes/ATOMICSELECTION html_attribute|'''ATOMICSELECTION''']]
|Specifies whether the element and its contents must be selected as a whole, indivisible unit.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[html/attributes/border (frameSet, iframe)|'''border''']]
|Sets or retrieves the space between the frames, including the 3-D border.
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
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[dom/properties/contentDocument|'''contentDocument''']]
|Retrieves the [[dom/document|'''document''']] object of the page or frame.
|-
|[[dom/properties/contentWindow|'''contentWindow''']]
|Retrieves the 
object of the specified 
.
|-
|[[html/attributes/dataFld|'''dataFld''']]
|Sets or retrieves a field of a given data source, as specified by the [[html/attributes/dataSrc|'''dataSrc''']] property, to bind to the specified object.
|-
|[[html/attributes/dataSrc|'''dataSrc''']]
|Sets or retrieves the source of the data for data binding.
|-
|[[dom/properties/firstChild|'''firstChild''']]
|Gets a reference to the first child in the [[dom/properties/childNodes|'''childNodes''']] collection of the object.
|-
|[[dom/traversal/properties/firstElementChild|'''firstElementChild''']]
|Retrieves a reference to the first child element, or NULL if there are no child elements.
|-
|[[html/attributes/frameBorder|'''frameBorder''']]
|Sets or retrieves whether to display a border for the frame.
|-
|[[html/attributes/frameSpacing|'''frameSpacing''']]
|Sets or retrieves the amount of additional space between the frames.
|-
|[[html/attributes/height|'''height''']]
|Sets or retrieves the height of the object.
|-
|[[html/attributes/hideFocus|'''hideFocus''']]
|Sets or gets the value that indicates whether the object visibly shows that it has focus.
|-
|[[html/attributes/hspace|'''hspace''']]
|Sets or retrieves the horizontal margin for the object.
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
|[[html/attributes/longDesc|'''longDesc''']]
|Sets or retrieves a URI to a long description of the object.
|-
|[[html/attributes/marginHeight|'''marginHeight''']]
|Sets or retrieves the top and bottom margin heights before displaying the text in a frame.
|-
|[[html/attributes/marginWidth|'''marginWidth''']]
|Sets or retrieves the left and right margin widths before displaying the text in a frame.
|-
|[[html/attributes/name (frames)|'''name''']]
|Sets or retrieves the frame name.
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
|[[html/attributes/noResize|'''noResize''']]
|Sets or retrieves whether the user can resize the frame.
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
|[[dom/properties/readyState|'''readyState''']]
|Retrieves the current state of the object.
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
|[[html/attributes/sandbox|'''sandbox''']]
|Enables security restrictions for '''iframe''' elements that contain potentially untrusted content.
|-
|'''scopeName'''
|Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
|-
|[[html/attributes/scrolling|'''scrolling''']]
|Sets or retrieves whether the frame can be scrolled.
|-
|[[html/attributes/security html_attribute|'''security''']]
|Sets the value indicating whether the source file of a '''frame''' or '''iframe''' has specific security restrictions applied. 

This attribute is not supported for     Metro style apps using JavaScript.
|-
|[[dom/properties/sourceIndex|'''sourceIndex''']]
|Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|'''all''']] collection.
|-
|[[html/attributes/src (iframe, embed, xml)|'''src''']]
|Sets or retrieves a URL to be loaded by the object.
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
|[[dom/properties/uniqueID|'''uniqueID''']]
|Retrieves an autogenerated, unique identifier for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|-
|[[html/attributes/vspace|'''vspace''']]
|Sets or retrieves the vertical margin for the object.
|-
|[[html/attributes/width|'''width''']]
|Sets or retrieves the width of the  object.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Using IFRAME Elements</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}