{{Page_Title|big}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|'''big'''要素はbigタグで囲んだテキストが周囲のテキストより大きく表示されるべきであることを示します。
HTML5ではもうほとんど使われていませんので、代わりにCSSを使ってください。
}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=以下の例は'''BIG'''を使ってテキストを強調しています。
|Code=こっちの文字よりも&lt;BIG&gt;こっちの文字のほうが大きい&lt;/BIG&gt;。
}}
}}
{{Notes_Section
|Notes====備考===
|Import_Notes====標準情報===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 15.2.1


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|inline
|}

===Members===
The '''big''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''big''' object has these events.
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
The '''big''' object has these methods.
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
|[[dom/methods/getElementsByTagName|'''getElementsByTagName''']]
|Retrieves a collection of objects based on the specified element name.
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
The '''big''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/accessKey|'''accessKey''']]
|Sets or retrieves the access key for the object.
|-
|[[css/properties/animation/animation|'''animation''']]
|Gets or sets one or more shorthand values  that specify all animation properties (except   [[css/properties/animation-play-state|'''animation-play-state''']]) for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animation-name''']] property.
|-
|[[css/properties/animation-delay|'''animationDelay''']]
|Gets or sets one or more values  that specify the offset within an animation cycle (the amount of time from the start of a cycle) before  the animation  is displayed  for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animation-name''']] property.
|-
|[[css/properties/animation-direction|'''animationDirection''']]
|Gets or sets one or more values  that specify the direction of play for an animation cycle.
|-
|[[css/properties/animation-duration|'''animationDuration''']]
|Gets or sets one or more values that specify the length of time to complete one cycle of the animation.
|-
|[[css/properties/animation-fill-mode|'''animationFillMode''']]
|Gets or sets one or more values  that specify whether the effects of an animation are visible before or after it plays.
|-
|[[css/properties/animation-iteration-count|'''animationIterationCount''']]
|Gets or sets one or more values  that specify the number of times an animation cycle is played.
|-
|[[css/properties/animation-name|'''animationName''']]
|Gets or sets a value  that identifies one or more animation names. An animation name identifies (or selects) a  CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule.
|-
|[[css/properties/animation-play-state|'''animationPlayState''']]
|Gets or sets one or more values  that specify whether an animation is playing or paused.
|-
|[[css/properties/animation-timing-function|'''animationTimingFunction''']]
|Gets or sets one or more values  that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes|'''@keyframes''']] at-rule specified by the [[css/properties/animation-name|'''animationName''']] property.
|-
|[[html/attributes/ATOMICSELECTION html_attribute|'''ATOMICSELECTION''']]
|Specifies whether the element and its contents must be selected as a whole, indivisible unit.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[css/properties/backface-visibility|'''backfaceVisibility''']]
|Gets or sets a value  that specifies whether the back face (reverse side) of an  object is visible.
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
|[[html/attributes/contentEditable|'''contentEditable''']]
|Sets or retrieves the string that indicates whether the user can edit the content of the object.
|-
|[[html/attributes/dir|'''dir''']]
|Sets or retrieves the reading order of the object.
|-
|[[dom/properties/firstChild|'''firstChild''']]
|Gets a reference to the first child in the [[dom/properties/childNodes|'''childNodes''']] collection of the object.
|-
|[[dom/traversal/properties/firstElementChild|'''firstElementChild''']]
|Retrieves a reference to the first child element, or null if there are no child elements.
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
|Retrieves a reference to the last child element or null if there are no child elements.
|-
|[[css/properties/ms-grid-column|'''msGridColumn''']]
|Gets or sets a value  that specifies in which column of the grid to place the object.
|-
|[[css/properties/ms-grid-column-align|'''msGridColumnAlign''']]
|Gets or sets a value  that specifies the horizontal alignment of the object within the  grid column.
|-
|[[css/properties/ms-grid-columns|'''msGridColumns''']]
|Gets or sets one or more values that specify the width of each grid column within the object.
|-
|[[css/properties/ms-grid-column-span|'''msGridColumnSpan''']]
|Gets or sets a value  that specifies the number of  columns of the grid that the object spans.
|-
|[[css/properties/ms-grid-row|'''msGridRow''']]
|Gets or sets a value  that specifies in which row of the grid to place the object.
|-
|[[css/properties/ms-grid-row-align|'''msGridRowAlign''']]
|Gets or sets a value  that specifies the vertical alignment of the object within the  grid row.
|-
|[[css/properties/ms-grid-rows|'''msGridRows''']]
|Gets or sets one or more values  that specify the height of each grid row within the object.
|-
|[[css/properties/ms-grid-row-span|'''msGridRowSpan''']]
|Gets or sets a value  that specifies the number of  rows of the grid that the object spans.
|-
|[[dom/traversal/properties/nextElementSibling|'''nextElementSibling''']]
|Retrieves a reference to the sibling element that immediately follows or null if the element does not have any sibling elements that follow it.
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
|[[css/properties/perspective|'''perspective''']]
|Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
|-
|[[css/properties/perspective-origin|'''perspectiveOrigin''']]
|Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an [[css/properties/perspective|'''perspective''']] property declaration.
|-
|[[dom/traversal/properties/previousElementSibling|'''previousElementSibling''']]
|Retrieves a reference to the immediately preceding sibling element or null if the element does not have any preceding siblings.
|-
|[[dom/properties/previousSibling|'''previousSibling''']]
|Gets a reference to the previous child of the parent for the object.
|-
|[[dom/properties/readyState|'''readyState''']]
|Retrieves the current state of the object.
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
|[[html/attributes/title|'''title''']]
|Sets or retrieves advisory information (a ToolTip) for the object.
|-
|[[css/properties/transform-style|'''transformStyle''']]
|Gets or sets a value  that specifies how child elements of the object are rendered in 3-D space.
|-
|[[css/properties/transition|'''transition''']]
|Gets or sets one or more shorthand values  that specify the transition properties  for a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-delay|'''transitionDelay''']]
|Gets or sets one or more values  that specify the offset within a transition (the amount of time from the start of a transition) before  the transition  is displayed  for a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-duration|'''transitionDuration''']]
|Gets or sets one or more values  that specify the durations of transitions on a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[css/properties/transition-property|'''transitionProperty''']]
|Gets or sets a value  that identifies the CSS property name or names to which the transition effect (defined by [[css/properties/transition-duration|'''transition-duration''']], [[css/functions/transition-timing-function|'''transition-timing-function''']], and [[css/properties/transition-delay|'''transition-delay''']]) is applied when a new property value is specified.
|-
|[[css/functions/transition-timing-function|'''transitionTimingFunction''']]
|Gets or sets one or more values  that specify the intermediate property values to be used during a transition on a set of corresponding object properties  identified in the [[css/properties/transition-property|'''transition-property''']] property.
|-
|[[dom/properties/uniqueID|'''uniqueID''']]
|Retrieves an autogenerated, unique identifier for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}