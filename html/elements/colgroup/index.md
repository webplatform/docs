{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''COLGROUP''' element to assign specific characteristics to two groups of columns in a table.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX1.htm
|Code=
&lt;html&gt;
&lt;body&gt;
&lt;table border{{=}}"2" rules{{=}}"groups"&gt;
    &lt;!-- RULES is set to "groups", which places internal dividing lines around 
table columns defined by COLGROUP. --&gt;
    &lt;colgroup span{{=}}"2" style{{=}}"color: red"&gt;
    &lt;/colgroup&gt;
    &lt;colgroup style{{=}}"color: blue"&gt;
    &lt;/colgroup&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
{{Single_Example
|Description=When '''COL''' elements are nested inside a '''COLGROUP''' element, the attributes of the '''COL''' elements override the attributes of the '''COLGROUP''' element. In this example, the last column has no formatting even though '''COLGROUP''' spans over all three columns. This happens because the [[html/attributes/span|'''SPAN''']] attribute of the nested '''COL''' element overrides the '''SPAN''' attribute of the '''COLGROUP'''.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX2.htm
|Code=
&lt;html&gt;
&lt;body&gt;
&lt;table border{{=}}"2"&gt;
    &lt;colgroup span{{=}}"3" style{{=}}"color: green; background: black"&gt;
        &lt;!-- Styling is applied to only the first two columns, instead of all
    three, and the font color is red instead of green. This is consistent
    with the attributes of the COL element. --&gt;
        &lt;col span{{=}}"2" style{{=}}"color: red"&gt;
    &lt;/colgroup&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the first group.&lt;/td&gt;
        &lt;td&gt;This column is in the second group.&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Nested '''COL''' elements override '''COLGROUP''' elements.
Use the [[html/attributes/span|'''SPAN''']] attribute to specify the number of table columns that the '''COLGROUP''' defines. This attribute has a default value equal to one.
'''COL''' elements can occur outside of a '''COLGROUP''' element, and these two elements can be used for similar purposes. However, you must use the '''COLGROUP''' element to determine where table internal dividing lines ([[html/attributes/rules|'''rules''']]) should go. This is illustrated in the first example .
You should avoid using the [[html/attributes/span|'''SPAN''']] attribute inside the '''COLGROUP''' element if there are '''COL''' elements nested within it. This is because the '''SPAN''' attribute that belongs to the nested '''COL''' elements will override the attribute that belongs to the '''COLGROUP''' element. This can cause confusing code and possibly unintended results. This behavior is illustrated in the second example.
The [[html/elements/table|'''table''']] object and its associated elements have a separate table object model, which uses different methods than the general object model. For more information on the table object model, see Building Tables Dynamically.
Windows Internet Explorer 8 will only render tables up to 1000 columns. To force Windows Internet Explorer 7 rendering mode, see How Do I Take Advantage of the New Features in Internet Explorer 8.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 11.2.4


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
The '''colGroup''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''colGroup''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/afterupdate|'''onafterupdate''']]
|Fires on a databound object after successfully updating the associated data in the data source object.
|-
|[[dom/events/beforecopy|'''onbeforecopy''']]
|Fires on the source object before the selection is copied to the system clipboard.
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
|[[dom/events/dataavailable|'''ondataavailable''']]
|Fires periodically as data arrives from data source objects that asynchronously transmit their data.
|-
|[[dom/events/datasetchanged|'''ondatasetchanged''']]
|Fires when the data set exposed by a data source object changes.
|-
|[[dom/events/datasetcomplete|'''ondatasetcomplete''']]
|Fires to indicate that all data is available from the data source object.
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
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/layoutcomplete|'''onlayoutcomplete''']]
|Fires when the print or print preview layout process finishes filling the current LayoutRect object with content from the source document.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
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
The '''colGroup''' object has these methods.
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
The '''colGroup''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/align|'''align''']]
|Sets or retrieves the alignment of the object relative to the display or table.
|-
|[[html/attributes/ATOMICSELECTION html_attribute|'''ATOMICSELECTION''']]
|Specifies whether the element and its contents must be selected as a whole, indivisible unit.
|-
|[[dom/properties/attributes|'''attributes''']]
|Retrieves a collection of attributes of the object.
|-
|[[html/attributes/BGCOLOR html_attribute|'''BGCOLOR''']]
|Sets the background color behind an object.
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
|[[html/attributes/dir|'''dir''']]
|Sets or retrieves the reading order of the object.
|-
|[[dom/properties/firstChild|'''firstChild''']]
|Gets a reference to the first child in the [[dom/properties/childNodes|'''childNodes''']] collection of the object.
|-
|[[dom/traversal/properties/firstElementChild|'''firstElementChild''']]
|Retrieves a reference to the first child element, or null if there are no child elements.
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
|[[html/attributes/span|'''span''']]
|Sets or retrieves the number of columns in the group.
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
|[[html/attributes/title|'''title''']]
|Sets or retrieves advisory information (a ToolTip) for the object.
|-
|[[dom/properties/uniqueID|'''uniqueID''']]
|Retrieves an autogenerated, unique identifier for the object.
|-
|[[dom/properties/uniqueNumber|'''uniqueNumber''']]
|Retrieves the element's unique number.
|-
|[[html/attributes/vAlign|'''vAlign''']]
|Sets or retrieves how text and other content are vertically aligned within the object that contains them.
|-
|[[html/attributes/width|'''width''']]
|Sets or retrieves the width of the  object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>col</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}