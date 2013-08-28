{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The script element enables dynamic script and data blocks to be included in documents.}}
{{Markup_Element
|DOM_interface=dom/HTMLScriptElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code snippet provides a scenario where an error occurs.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;SCRIPT LANGUAGE{{=}}"XML" id{{=}}"mySrc1"&gt;
&lt;offerings&gt;
 &lt;class&gt;&lt;materials&gt;This should render.&lt;/materials&gt;&lt;time&gt;1.5
hr&lt;/time&gt;&lt;/class&gt;
&lt;/offerings&gt;
&lt;/SCRIPT&gt;
&lt;SCRIPT LANGUAGE{{=}}"javascript"&gt;
function returnIslandRootName()
{
  var islandRoot {{=}} document.all["mySrc1"].XMLDocument;
  console.log(islandRoot.nodeName);
}
&lt;/SCRIPT&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;button onclick{{=}}"returnIslandRootName()"&gt;Test the XML Data Island&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Description=Because the XML data island is the first instance of the '''script''' object that has the [[html/attributes/language|'''language''']] attribute defined, ''MSHTML'' attempts to locate the <code>returnIslandRootName</code> function in the XML and fails. To correct the sample, the order of the '''script''' objects can change, as shown by the following example:
|Code=&lt;html&gt;
&lt;head&gt;
&lt;SCRIPT LANGUAGE{{=}}"javascript"&gt;
function returnIslandRootName()
{
  var islandRoot {{=}} document.all["mySrc1"].XMLDocument;
  console.log(islandRoot.nodeName);
}
&lt;/SCRIPT&gt;
&lt;SCRIPT LANGUAGE{{=}}"XML" id{{=}}"mySrc1"&gt;
&lt;offerings&gt;
 &lt;class&gt;&lt;materials&gt;This should render.&lt;/materials&gt;&lt;time&gt;1.5
hr&lt;/time&gt;&lt;/class&gt;
&lt;/offerings&gt;
&lt;/SCRIPT&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;button onclick{{=}}"returnIslandRootName()"&gt;Test the XML Data Island&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Code within the '''script''' block that is not contained within a function is executed immediately as the document is loaded. To keep scripts from being displayed, nest the '''script''' block within a '''comment''' block.
Script appearing after a '''frameSet''' element is ignored.
Whenever the [[html/attributes/language|'''language''']] attribute is not defined on the '''script''' object, then ''MSHTML'' attempts to select a suitable scripting engine. An error generally occurs if the wrong scripting engine is selected. When more than one '''script''' object is used in a document, it can be necessary to specify the ''language'' attribute for each '''script''' object, and doing so is always recommended. The order of the '''script''' objects in a document can also be important, especially if scripting event handlers are assigned to one or more elements in the document. XML is legitimate content for the '''script''' object, but XML is not a scripting language. Therefore, an error can occur if ''MSHTML'' selects an XML data island as the '''script''' object that contains an event handler function. This can happen because ''MSHTML'' selects the first '''script''' object that has the '''language''' attribute defined as the default script block for event handlers. For more information, see the examples.
Windows Internet Explorer 8 and later. The value of the [[html/attributes/src (script)|'''src''']] attribute depends on the current document compatibility mode.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.1


===Members===
The '''script''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''script''' object has these events.
{{{!}} class="wikitable"
{{!}}-
!Event
!Description
{{!}}-
{{!}}[[dom/events/abort{{!}}'''onabort''']]
{{!}}Fires when the user aborts the download.
{{!}}-
{{!}}[[dom/events/afterupdate{{!}}'''onafterupdate''']]
{{!}}Fires on a databound object after successfully updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/beforecopy{{!}}'''onbeforecopy''']]
{{!}}Fires on the source object before the selection is copied to the system clipboard.
{{!}}-
{{!}}[[dom/events/beforeupdate{{!}}'''onbeforeupdate''']]
{{!}}Fires on a databound object before updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/cellchange{{!}}'''oncellchange''']]
{{!}}Fires when data changes in the data provider.
{{!}}-
{{!}}[[dom/events/change{{!}}'''onchange''']]
{{!}}Fires when the contents of the object or selection have changed.
{{!}}-
{{!}}[[dom/events/dataavailable{{!}}'''ondataavailable''']]
{{!}}Fires periodically as data arrives from data source objects that asynchronously transmit their data.
{{!}}-
{{!}}[[dom/events/datasetchanged{{!}}'''ondatasetchanged''']]
{{!}}Fires when the data set exposed by a data source object changes.
{{!}}-
{{!}}[[dom/events/datasetcomplete{{!}}'''ondatasetcomplete''']]
{{!}}Fires to indicate that all data is available from the data source object.
{{!}}-
{{!}}[[dom/events/error{{!}}'''onerror''']]
{{!}}Fires when an error occurs during object loading.
{{!}}-
{{!}}[[dom/events/errorupdate{{!}}'''onerrorupdate''']]
{{!}}Fires on a databound object when an error occurs while updating the associated data in the data source object.
{{!}}-
{{!}}[[dom/events/filterchange{{!}}'''onfilterchange''']]
{{!}}Fires when a visual filter changes state or completes a transition.
{{!}}-
{{!}}[[dom/events/input{{!}}'''oninput''']]
{{!}}Occurs when the text content of an element is changed through the user interface.
{{!}}-
{{!}}[[dom/events/layoutcomplete{{!}}'''onlayoutcomplete''']]
{{!}}Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
{{!}}-
{{!}}[[dom/events/load{{!}}'''onload''']]
{{!}}Fires immediately after the client loads the object.
{{!}}-
{{!}}[[dom/events/propertychange{{!}}'''onpropertychange''']]
{{!}}Fires when a property changes on the object.
{{!}}-
{{!}}[[dom/events/readystatechange{{!}}'''onreadystatechange''']]
{{!}}Fires when the state of the object has changed.
{{!}}-
{{!}}[[dom/events/reset{{!}}'''onreset''']]
{{!}}Fires when the user resets a form.
{{!}}-
{{!}}[[dom/events/resize{{!}}'''onresize''']]
{{!}}Fires when the size of the object is about to change.
{{!}}-
{{!}}[[dom/events/rowenter{{!}}'''onrowenter''']]
{{!}}Fires to indicate that the current row has changed in the data source and new data values are available on the object.
{{!}}-
{{!}}[[dom/events/rowexit{{!}}'''onrowexit''']]
{{!}}Fires just before the data source control changes the current row in the object.
{{!}}-
{{!}}[[dom/events/rowsdelete{{!}}'''onrowsdelete''']]
{{!}}Fires when rows are about to be deleted from the recordset.
{{!}}-
{{!}}[[dom/events/rowsinserted{{!}}'''onrowsinserted''']]
{{!}}Fires just after new rows are inserted in the current recordset.
{{!}}-
{{!}}[[dom/events/selectstart{{!}}'''onselect''']]
{{!}}Fires when the current selection changes.
{{!}}}
 

====Methods====
The '''script''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''addBehavior'''
{{!}}Attaches a behavior to the element. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/applyElement{{!}}'''applyElement''']]
{{!}}Makes the element either a child or parent of another element.
{{!}}-
{{!}}[[dom/methods/attachEvent{{!}}'''attachEvent''']]
{{!}}Binds the specified function to an event, so that the function gets called whenever the event fires on the object.
{{!}}-
{{!}}[[dom/methods/clearAttributes{{!}}'''clearAttributes''']]
{{!}}Removes all attributes and values from the object.
{{!}}-
{{!}}[[dom/methods/cloneNode{{!}}'''cloneNode''']]
{{!}}Copies a reference to the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/componentFromPoint{{!}}'''componentFromPoint''']]
{{!}}Returns the component located at the specified coordinates via certain events.
{{!}}-
{{!}}[[dom/methods/detachEvent{{!}}'''detachEvent''']]
{{!}}Unbinds the specified function from the event, so that the function stops receiving notifications when the event fires.
{{!}}-
{{!}}[[dom/methods/doScroll{{!}}'''doScroll''']]
{{!}}Simulates a click on a scroll bar component.
{{!}}-
{{!}}[[dom/methods/dragDrop{{!}}'''dragDrop''']]
{{!}}Initiates a drag event.
{{!}}-
{{!}}[[dom/methods/fireEvent{{!}}'''fireEvent''']]
{{!}}Fires a specified event on the object.
{{!}}-
{{!}}[[dom/methods/getAdjacentText{{!}}'''getAdjacentText''']]
{{!}}Returns the adjacent text string.
{{!}}-
{{!}}[[dom/methods/getAttribute{{!}}'''getAttribute''']]
{{!}}Retrieves the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/getAttributeNode{{!}}'''getAttributeNode''']]
{{!}}Retrieves an [[dom/attributes{{!}}'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name{{!}}'''name''']] property.
{{!}}-
{{!}}[[dom/methods/getAttributeNodeNS{{!}}'''getAttributeNodeNS''']]
{{!}}Gets an [[dom/attributes{{!}}'''attribute''']] object that matches the specified namespace and name.
{{!}}-
{{!}}[[dom/methods/getAttributeNS{{!}}'''getAttributeNS''']]
{{!}}Gets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/getElementsByClassName{{!}}'''getElementsByClassName''']]
{{!}}Gets a collection of objects that are based on the value of the [[dom/properties/className{{!}}'''CLASS''']] attribute.
{{!}}-
{{!}}[[dom/methods/getElementsByTagName{{!}}'''getElementsByTagName''']]
{{!}}Retrieves a collection of objects based on the specified element name.
{{!}}-
{{!}}[[dom/methods/getElementsByTagNameNS{{!}}'''getElementsByTagNameNS''']]
{{!}}Gets a collection of objects that are based on the specified element names within a specified namespace.
{{!}}-
{{!}}[[dom/methods/hasAttribute{{!}}'''hasAttribute''']]
{{!}}Determines whether an attribute with the specified name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributeNS{{!}}'''hasAttributeNS''']]
{{!}}Determines whether an attribute that has the specified namespace and name exists.
{{!}}-
{{!}}[[dom/methods/hasAttributes{{!}}'''hasAttributes''']]
{{!}}Determines whether one or more attributes exist for the object.
{{!}}-
{{!}}[[dom/methods/hasChildNodes{{!}}'''hasChildNodes''']]
{{!}}Returns a value that indicates whether the object has children.
{{!}}-
{{!}}[[dom/methods/insertAdjacentElement{{!}}'''insertAdjacentElement''']]
{{!}}Inserts an element at the specified location.
{{!}}-
{{!}}[[dom/methods/mergeAttributes{{!}}'''mergeAttributes''']]
{{!}}Copies all read/write attributes to the specified element.
{{!}}-
{{!}}[[dom/methods/matchesSelector{{!}}'''msMatchesSelector''']]
{{!}}Determines whether an object matches the specified selector.
{{!}}-
{{!}}[[dom/methods/normalize{{!}}'''normalize''']]
{{!}}Merges adjacent DOM objects to produce a normalized document object model.
{{!}}-
{{!}}[[dom/methods/removeAttribute{{!}}'''removeAttribute''']]
{{!}}Removes an attribute from an object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNode{{!}}'''removeAttributeNode''']]
{{!}}Removes an [[dom/attributes{{!}}'''attribute''']] object from the object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNS{{!}}'''removeAttributeNS''']]
{{!}}Removes the specified attribute from the object.
{{!}}-
{{!}}'''removeBehavior'''
{{!}}Detaches a behavior from the element.
{{!}}-
{{!}}[[dom/methods/removeNode{{!}}'''removeNode''']]
{{!}}Removes the object from the document hierarchy.
{{!}}-
{{!}}[[dom/methods/replaceAdjacentText{{!}}'''replaceAdjacentText''']]
{{!}}Replaces the text adjacent to the element.
{{!}}-
{{!}}[[dom/methods/replaceNode{{!}}'''replaceNode''']]
{{!}}Replaces the object with another element.
{{!}}-
{{!}}[[dom/methods/setActive{{!}}'''setActive''']]
{{!}}Sets the object as active without setting focus to the object.
{{!}}-
{{!}}[[dom/methods/setAttribute{{!}}'''setAttribute''']]
{{!}}Sets the value of the specified attribute.
{{!}}-
{{!}}[[dom/methods/setAttributeNode{{!}}'''setAttributeNode''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object node as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNodeNS{{!}}'''setAttributeNodeNS''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNS{{!}}'''setAttributeNS''']]
{{!}}Sets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/setCapture{{!}}'''setCapture''']]
{{!}}Sets the mouse capture to the object that belongs to the current document.
{{!}}-
{{!}}[[dom/methods/swapNode{{!}}'''swapNode''']]
{{!}}Exchanges the location of two objects in the document hierarchy.
{{!}}}
 

====Properties====
The '''script''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[css/properties/animation/animation{{!}}'''animation''']]
{{!}}Gets or sets one or more shorthand values  that specify all animation properties (except   [[css/properties/animation-play-state{{!}}'''animation-play-state''']]) for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animation-name''']] property.
{{!}}-
{{!}}[[css/properties/animation-delay{{!}}'''animationDelay''']]
{{!}}Gets or sets one or more values  that specify the offset within an animation cycle (the amount of time from the start of a cycle) before  the animation  is displayed  for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animation-name''']] property.
{{!}}-
{{!}}[[css/properties/animation-direction{{!}}'''animationDirection''']]
{{!}}Gets or sets one or more values  that specify the direction of play for an animation cycle.
{{!}}-
{{!}}[[css/properties/animation-duration{{!}}'''animationDuration''']]
{{!}}Gets or sets one or more values that specify the length of time to complete one cycle of the animation.
{{!}}-
{{!}}[[css/properties/animation-fill-mode{{!}}'''animationFillMode''']]
{{!}}Gets or sets one or more values  that specify whether the effects of an animation are visible before or after it plays.
{{!}}-
{{!}}[[css/properties/animation-iteration-count{{!}}'''animationIterationCount''']]
{{!}}Gets or sets one or more values  that specify the number of times an animation cycle is played.
{{!}}-
{{!}}[[css/properties/animation-name{{!}}'''animationName''']]
{{!}}Gets or sets a value  that identifies one or more animation names. An animation name identifies (or selects) a  CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule.
{{!}}-
{{!}}[[css/properties/animation-play-state{{!}}'''animationPlayState''']]
{{!}}Gets or sets one or more values  that specify whether an animation is playing or paused.
{{!}}-
{{!}}[[css/properties/animation-timing-function{{!}}'''animationTimingFunction''']]
{{!}}Gets or sets one or more values  that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animationName''']] property.
{{!}}-
{{!}}[[dom/properties/attributes{{!}}'''attributes''']]
{{!}}Retrieves a collection of attributes of the object.
{{!}}-
{{!}}[[css/properties/backface-visibility{{!}}'''backfaceVisibility''']]
{{!}}Gets or sets a value  that specifies whether the back face (reverse side) of an  object is visible.
{{!}}-
{{!}}[[css/properties/break-after{{!}}'''breakAfter''']]
{{!}}Gets or sets the column-break behavior that follows a content block in a multi-column element.
{{!}}-
{{!}}[[css/properties/break-before{{!}}'''breakBefore''']]
{{!}}Gets or sets the column-break behavior that precedes a content block in a multi-column element.
{{!}}-
{{!}}[[css/properties/break-inside{{!}}'''breakInside''']]
{{!}}Gets or sets the column-break behavior that occurs within a content block in a multi-column element.
{{!}}-
{{!}}[[dom/properties/canHaveChildren{{!}}'''canHaveChildren''']]
{{!}}Gets a value indicating whether the object can contain child objects.
{{!}}-
{{!}}[[dom/properties/canHavedom/canHaveHTML{{!}}'''canHaveHTML''']]
{{!}}Retrieves the value indicating whether the object can contain rich HTML markup.
{{!}}-
{{!}}[[dom/properties/charset{{!}}'''charset''']]
{{!}}Sets or retrieves the character set used to encode the object.
{{!}}-
{{!}}[[dom/traversal/properties/childElementCount{{!}}'''childElementCount''']]
{{!}}Retrieves the number of immediate child nodes of the current element or a zero if the element does not contain any child nodes. [[dom/traversal/properties/childElementCount{{!}}'''childElementCount''']] does not return all child nodes, only child nodes that are [[dom/properties/nodeType{{!}}'''nodeType''']] {{=}}1, or element nodes.
{{!}}-
{{!}}[[dom/properties/clientHeight{{!}}'''clientHeight''']]
{{!}}Retrieves the height of the object including padding, but not including margin, border, or scroll bar.
{{!}}-
{{!}}[[dom/properties/clientLeft{{!}}'''clientLeft''']]
{{!}}Retrieves the distance between the [[dom/properties/offsetLeft{{!}}'''offsetLeft''']] property and the true left side of the client area.
{{!}}-
{{!}}[[dom/properties/clientTop{{!}}'''clientTop''']]
{{!}}Retrieves the distance between the [[dom/properties/offsetTop{{!}}'''offsetTop''']] property and the true top of the client area.
{{!}}-
{{!}}[[dom/properties/clientWidth{{!}}'''clientWidth''']]
{{!}}Retrieves the width of the object including padding, but not including margin, border, or scroll bar.
{{!}}-
{{!}}[[css/properties/column-count{{!}}'''columnCount''']]
{{!}}Gets or sets the optimal number of columns in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-fill{{!}}'''columnFill''']]
{{!}}Gets or sets a value that indicates how the column lengths in a multi-column element are affected by the content flow.
{{!}}-
{{!}}[[css/properties/column-gap{{!}}'''columnGap''']]
{{!}}Gets or sets the width of the gap between columns in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-rule{{!}}'''columnRule''']]
{{!}}Gets or sets a shorthand value  that specifies values for the [[css/properties/column-rule-width{{!}}'''columnRuleWidth''']],  [[css/properties/column-rule-style{{!}}'''columnRuleStyle''']], and the [[css/properties/column-rule-color{{!}}'''columnRuleColor''']] of a multi-column element.
{{!}}-
{{!}}[[css/properties/column-rule-color{{!}}'''columnRuleColor''']]
{{!}}Gets or sets the color for all column rules in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-rule-style{{!}}'''columnRuleStyle''']]
{{!}}Gets or sets the style for all column rules in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-rule-width{{!}}'''columnRuleWidth''']]
{{!}}Gets or sets  the width of all column rules in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-span{{!}}'''columnSpan''']]
{{!}}Gets or sets the number of columns that a content block spans in a multi-column element.
{{!}}-
{{!}}[[css/properties/column-width{{!}}'''columnWidth''']]
{{!}}Gets or sets the optimal width of the columns in a multi-column element.
{{!}}-
{{!}}[[dom/properties/constructor{{!}}'''constructor''']]
{{!}}Returns a reference to the constructor of an object.
{{!}}-
{{!}}[[html/attributes/defer{{!}}'''defer''']]
{{!}}Sets or retrieves the status of the script.
{{!}}-
{{!}}[[html/attributes/event{{!}}'''event''']]
{{!}}Sets or retrieves the event for which the script is written.
{{!}}-
{{!}}[[dom/properties/firstChild{{!}}'''firstChild''']]
{{!}}Gets a reference to the first child in the [[dom/properties/childNodes{{!}}'''childNodes''']] collection of the object.
{{!}}-
{{!}}[[dom/traversal/properties/firstElementChild{{!}}'''firstElementChild''']]
{{!}}Retrieves a reference to the first child element, or NULL if there are no child elements.
{{!}}-
{{!}}[[html/attributes/dom/htmlFor{{!}}'''htmlFor''']]
{{!}}Sets or retrieves the object that is bound to the event script.
{{!}}-
{{!}}[[html/attributes/id{{!}}'''id''']]
{{!}}Sets or retrieves the string identifying the object.
{{!}}-
{{!}}[[dom/properties/isContentEditable{{!}}'''isContentEditable''']]
{{!}}Gets the value that indicates whether the user can edit the contents of the object.
{{!}}-
{{!}}[[dom/properties/isDisabled{{!}}'''isDisabled''']]
{{!}}Gets the value that indicates whether the user can interact with the object.
{{!}}-
{{!}}[[dom/properties/isMultiLine{{!}}'''isMultiLine''']]
{{!}}Retrieves the value indicating whether the content of the object contains one or more lines.
{{!}}-
{{!}}[[dom/properties/lastChild{{!}}'''lastChild''']]
{{!}}Gets a reference to the last child in the [[dom/properties/childNodes{{!}}'''childNodes''']] collection of an object.
{{!}}-
{{!}}[[dom/traversal/properties/lastElementChild{{!}}'''lastElementChild''']]
{{!}}Retrieves a reference to the last child element or NULL if there are no child elements.
{{!}}-
{{!}}[[css/properties/ms-grid-column{{!}}'''msGridColumn''']]
{{!}}Gets or sets a value  that specifies in which column of the grid to place the object.
{{!}}-
{{!}}[[css/properties/ms-grid-column-align{{!}}'''msGridColumnAlign''']]
{{!}}Gets or sets a value  that specifies the horizontal alignment of the object within the  grid column.
{{!}}-
{{!}}[[css/properties/ms-grid-columns{{!}}'''msGridColumns''']]
{{!}}Gets or sets one or more values that specify the width of each grid column within the object.
{{!}}-
{{!}}[[css/properties/ms-grid-column-span{{!}}'''msGridColumnSpan''']]
{{!}}Gets or sets a value  that specifies the number of  columns of the grid that the object spans.
{{!}}-
{{!}}[[css/properties/ms-grid-row{{!}}'''msGridRow''']]
{{!}}Gets or sets a value  that specifies in which row of the grid to place the object.
{{!}}-
{{!}}[[css/properties/ms-grid-row-align{{!}}'''msGridRowAlign''']]
{{!}}Gets or sets a value  that specifies the vertical alignment of the object within the  grid row.
{{!}}-
{{!}}[[css/properties/ms-grid-rows{{!}}'''msGridRows''']]
{{!}}Gets or sets one or more values  that specify the height of each grid row within the object.
{{!}}-
{{!}}[[css/properties/ms-grid-row-span{{!}}'''msGridRowSpan''']]
{{!}}Gets or sets a value  that specifies the number of  rows of the grid that the object spans.
{{!}}-
{{!}}[[dom/traversal/properties/nextElementSibling{{!}}'''nextElementSibling''']]
{{!}}Retrieves a reference to the sibling element that immediately follows or NULL if the element does not have any sibling elements that follow it.
{{!}}-
{{!}}[[dom/properties/nextSibling{{!}}'''nextSibling''']]
{{!}}Retrieves a reference to the next child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/nodeName{{!}}'''nodeName''']]
{{!}}Gets the name of a particular type of node.
{{!}}-
{{!}}[[dom/properties/nodeType{{!}}'''nodeType''']]
{{!}}Retrieves the type of the requested node.
{{!}}-
{{!}}[[dom/properties/nodeValue{{!}}'''nodeValue''']]
{{!}}Gets or sets the value of a node.
{{!}}-
{{!}}[[dom/properties/ownerDocument{{!}}'''ownerDocument''']]
{{!}}Retrieves the [[dom/document{{!}}'''document''']] object associated with the node.
{{!}}-
{{!}}[[dom/properties/parentNode{{!}}'''parentNode''']]
{{!}}Retrieves the parent object in the document hierarchy.
{{!}}-
{{!}}[[css/properties/perspective{{!}}'''perspective''']]
{{!}}Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
{{!}}-
{{!}}[[css/properties/perspective-origin{{!}}'''perspectiveOrigin''']]
{{!}}Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an [[css/properties/perspective{{!}}'''perspective''']] property declaration.
{{!}}-
{{!}}[[dom/traversal/properties/previousElementSibling{{!}}'''previousElementSibling''']]
{{!}}Retrieves a reference to the immediately preceding sibling element or NULL if the element does not have any preceding siblings.
{{!}}-
{{!}}[[dom/properties/previousSibling{{!}}'''previousSibling''']]
{{!}}Gets a reference to the previous child of the parent for the object.
{{!}}-
{{!}}[[dom/properties/readyState (Link, Img, Input, Style...elements){{!}}'''readyState''']]
{{!}}Retrieves a value that indicates the current state of the object.
{{!}}-
{{!}}[[html/attributes/role{{!}}'''role''']]
{{!}}Sets or retrieves the role for this element.
{{!}}-
{{!}}'''scopeName'''
{{!}}Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/scrollHeight{{!}}'''scrollHeight''']]
{{!}}Retrieves the scrolling height of the object.
{{!}}-
{{!}}[[dom/properties/scrollLeft{{!}}'''scrollLeft''']]
{{!}}Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
{{!}}-
{{!}}[[dom/properties/scrollTop{{!}}'''scrollTop''']]
{{!}}Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
{{!}}-
{{!}}[[dom/properties/scrollWidth{{!}}'''scrollWidth''']]
{{!}}Retrieves the scrolling width of the object.
{{!}}-
{{!}}[[html/attributes/src (script){{!}}'''src''']]
{{!}}Retrieves the URL to an external file that contains the source code or data.
{{!}}-
{{!}}[[dom/properties/tagUrn{{!}}'''tagUrn''']]
{{!}}Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/text{{!}}'''text''']]
{{!}}Retrieves or sets the text of the object as a string.
{{!}}-
{{!}}[[css/properties/transform-style{{!}}'''transformStyle''']]
{{!}}Gets or sets a value  that specifies how child elements of the object are rendered in 3-D space.
{{!}}-
{{!}}[[css/properties/transition{{!}}'''transition''']]
{{!}}Gets or sets one or more shorthand values  that specify the transition properties  for a set of corresponding object properties  identified in the [[css/properties/transition-property{{!}}'''transition-property''']] property.
{{!}}-
{{!}}[[css/properties/transition-delay{{!}}'''transitionDelay''']]
{{!}}Gets or sets one or more values  that specify the offset within a transition (the amount of time from the start of a transition) before  the transition  is displayed  for a set of corresponding object properties  identified in the [[css/properties/transition-property{{!}}'''transition-property''']] property.
{{!}}-
{{!}}[[css/properties/transition-duration{{!}}'''transitionDuration''']]
{{!}}Gets or sets one or more values  that specify the durations of transitions on a set of corresponding object properties  identified in the [[css/properties/transition-property{{!}}'''transition-property''']] property.
{{!}}-
{{!}}[[css/properties/transition-property{{!}}'''transitionProperty''']]
{{!}}Gets or sets a value  that identifies the CSS property name or names to which the transition effect (defined by [[css/properties/transition-duration{{!}}'''transition-duration''']], [[css/functions/transition-timing-function{{!}}'''transition-timing-function''']], and [[css/properties/transition-delay{{!}}'''transition-delay''']]) is applied when a new property value is specified.
{{!}}-
{{!}}[[css/functions/transition-timing-function{{!}}'''transitionTimingFunction''']]
{{!}}Gets or sets one or more values  that specify the intermediate property values to be used during a transition on a set of corresponding object properties  identified in the [[css/properties/transition-property{{!}}'''transition-property''']] property.
{{!}}-
{{!}}[[html/attributes/type (script element){{!}}'''type''']]
{{!}}Sets or retrieves the MIME type for the associated scripting engine.
{{!}}-
{{!}}[[dom/properties/uniqueID{{!}}'''uniqueID''']]
{{!}}Retrieves an autogenerated, unique identifier for the object.
{{!}}-
{{!}}[[css/cssom/properties/usedCharset{{!}}'''usedCharset''']]
{{!}}Gets the character set used to decode the current document.
{{!}}}
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
*<code>XML Data Islands</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}