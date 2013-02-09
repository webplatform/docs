{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''hidden''' type of the [[html/elements/input|&lt;input&gt;]] element represents a value that is hidden from the user, but which is sent with the form data; the value can be set programatically.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This input type presents no control to the user, but sends the value of the [[html/attributes/value (select, option element)|'''value''']] property with the submitted form.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|forbidden
|-
!CSS Display
|
|}

===Members===
The '''input type{{=}}hidden''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''input type{{=}}hidden''' object has these events.
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
|[[dom/events/beforeeditfocus|'''onbeforeeditfocus''']]
|Fires before an object contained in an editable element enters a ''UI Activation'' state or when an editable container object is ''control selection''.
|-
|[[dom/events/beforeupdate|'''onbeforeupdate''']]
|Fires on a databound object before updating the associated data in the data source object.
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
|[[dom/events/losecapture|'''onlosecapture''']]
|Fires when the object loses the mouse capture.
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
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|}
 

====Methods====
The '''input type{{=}}hidden''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|'''addBehavior'''
|Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
|-
|[[dom/methods/applyElement|'''applyElement''']]
|Makes the element either a child or parent of another element.
|-
|[[dom/methods/attachEvent|'''attachEvent''']]
|Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
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
|[[dom/traversal/methods/createTextRange|'''createTextRange''']]
|Creates a [[dom/traversal/TextRange|'''TextRange''']] object for the element.
|-
|[[dom/methods/detachEvent|'''detachEvent''']]
|Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
|-
|[[dom/methods/doScroll|'''doScroll''']]
|Simulates a click on a scroll bar component.
|-
|[[dom/methods/fireEvent|'''fireEvent''']]
|Fires a specified event on the object.
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
|[[dom/methods/insertAdjacentElement|'''insertAdjacentElement''']]
|Inserts an element at the specified location.
|-
|[[dom/methods/insertAdjacentHTML|'''insertAdjacentHTML''']]
|Inserts the given HTML text into the element at the location.
|-
|[[dom/methods/insertAdjacentText|'''insertAdjacentText''']]
|Inserts the given text into the element at the specified location.
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
The '''input type{{=}}hidden''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
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
|[[dom/properties/className|'''className''']]
|Sets or retrieves the class of the object.
|-
|[[html/attributes/dataFld|'''dataFld''']]
|Sets or retrieves a field of a given data source, as specified by the [[html/attributes/dataSrc|'''dataSrc''']] property, to bind to the specified object.
|-
|[[html/attributes/dataSrc|'''dataSrc''']]
|Sets or retrieves the source of the data for data binding.
|-
|[[dom/properties/defaultValue|'''defaultValue''']]
|Sets or retrieves the initial contents of the object.
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
|[[dom/properties/localName|'''localName''']]
|Retrieves the local name of the fully qualified XML declaration for a node.
|-
|[[html/attributes/name|'''name''']]
|Sets or retrieves the name of the object.
|-
|[[dom/properties/namespaceURI|'''namespaceURI''']]
|Retrieves the namespace URI of the fully qualified XML declaration for a node.
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
|[[dom/properties/offsetParent|'''offsetParent''']]
|Retrieves a reference to the container object that defines the [[dom/properties/offsetTop|'''offsetTop''']] and [[dom/properties/offsetLeft|'''offsetLeft''']] properties of the object.
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
|[[dom/properties/sourceIndex|'''sourceIndex''']]
|Retrieves the ordinal position of the object, in source order, as the object appears in the document's [[dom/properties/all|'''all''']] collection.
|-
|[[html/attributes/STYLE html_attribute|'''STYLE''']]
|Sets an inline style for the element.
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
|[[html/attributes/value (input elements)|'''value''']]
|Sets or retrieves the displayed value for the control object.  This value is returned to the server when the control object is submitted.
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
*<code>Reference</code>
*<code>input</code>
*<code>input type{{=}}submit</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}