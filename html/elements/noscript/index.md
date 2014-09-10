{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent and Children information.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The HTML NoScript Element (<noscript>) defines a section of html to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=You must disable javascript for this to work.
|Code=<script>
    //Do stuff...
</script>
<noscript>
    Your browser doesn't support javascript!
</noscript>
|LiveURL=https://rawgithub.com/WebPlatformDocs/6364342/raw/47a37f3fe0d920a0c6a8a7974dca473589f1e4f5/dabblet.html
}}
}}
{{Notes_Section
|Notes=Browsers that don't support the noscript tag will render the content regardless of whether the javascript is supported
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.3.1


===HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}inline
{{!}}}

===Members===
The '''noScript''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''noScript''' object has these events.
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
The '''noScript''' object has these methods.
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
{{!}}[[dom/methods/clearAttributes{{!}}'''clearAttributes''']]
{{!}}Removes all attributes and values from the object.
{{!}}-
{{!}}[[dom/methods/componentFromPoint{{!}}'''componentFromPoint''']]
{{!}}Returns the component located at the specified coordinates via certain events.
{{!}}-
{{!}}[[dom/methods/doScroll{{!}}'''doScroll''']]
{{!}}Simulates a click on a scroll bar component.
{{!}}-
{{!}}[[dom/methods/fireEvent{{!}}'''fireEvent''']]
{{!}}Fires a specified event on the object.
{{!}}-
{{!}}[[dom/methods/getAttributeNode{{!}}'''getAttributeNode''']]
{{!}}Retrieves an [[dom/attributes{{!}}'''attribute''']] object referenced by the '''attribute'''.[[html/attributes/name{{!}}'''name''']] property.
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
{{!}}[[dom/methods/matchesSelector{{!}}'''msMatchesSelector''']]
{{!}}Determines whether an object matches the specified selector.
{{!}}-
{{!}}[[dom/methods/normalize{{!}}'''normalize''']]
{{!}}Merges adjacent DOM objects to produce a normalized document object model.
{{!}}-
{{!}}[[dom/methods/removeAttributeNode{{!}}'''removeAttributeNode''']]
{{!}}Removes an [[dom/attributes{{!}}'''attribute''']] object from the object.
{{!}}-
{{!}}[[dom/methods/removeAttributeNS{{!}}'''removeAttributeNS''']]
{{!}}Removes the specified attribute from the object.
{{!}}-
{{!}}'''removeBehavior'''
{{!}}Detaches a behavior from the element.
{{!}}-
{{!}}[[dom/methods/replaceAdjacentText{{!}}'''replaceAdjacentText''']]
{{!}}Replaces the text adjacent to the element.
{{!}}-
{{!}}[[dom/methods/setActive{{!}}'''setActive''']]
{{!}}Sets the object as active without setting focus to the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNode{{!}}'''setAttributeNode''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object node as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNodeNS{{!}}'''setAttributeNodeNS''']]
{{!}}Sets an [[dom/attributes{{!}}'''attribute''']] object as part of the object.
{{!}}-
{{!}}[[dom/methods/setAttributeNS{{!}}'''setAttributeNS''']]
{{!}}Sets the value of the specified attribute within the specified namespace.
{{!}}-
{{!}}[[dom/methods/setCapture{{!}}'''setCapture''']]
{{!}}Sets the mouse capture to the object that belongs to the current document.
{{!}}}
 

====Properties====
The '''noScript''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[css/properties/animation/animation{{!}}'''animation''']]
{{!}}Gets or sets one or more shorthand values  that specify all animation properties (except   [[css/properties/animation-play-state{{!}}'''animation-play-state''']]) for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animation-name''']] property.
{{!}}-
{{!}}[[css/properties/animation-delay{{!}}'''animationDelay''']]
{{!}}Gets or sets one or more values  that specify the offset within an animation cycle (the amount of time from the start of a cycle) before  the animation  is displayed  for a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animation-name''']] property.
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
{{!}}Gets or sets a value  that identifies one or more animation names. An animation name identifies (or selects) a  CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule.
{{!}}-
{{!}}[[css/properties/animation-play-state{{!}}'''animationPlayState''']]
{{!}}Gets or sets one or more values  that specify whether an animation is playing or paused.
{{!}}-
{{!}}[[css/properties/animation-timing-function{{!}}'''animationTimingFunction''']]
{{!}}Gets or sets one or more values  that specify the intermediate property values to be used during a single cycle of an animation on a set of corresponding object properties  identified in the CSS [[css/atrules/@keyframes{{!}}'''@keyframes''']] at-rule specified by the [[css/properties/animation-name{{!}}'''animationName''']] property.
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
{{!}}[[css/properties/perspective{{!}}'''perspective''']]
{{!}}Gets or sets a value  that represents the perspective from which all child elements of the object are viewed.
{{!}}-
{{!}}[[css/properties/perspective-origin{{!}}'''perspectiveOrigin''']]
{{!}}Gets or sets one or two values  that represent the origin (the vanishing point for the 3-D space) of an object with an [[css/properties/perspective{{!}}'''perspective''']] property declaration.
{{!}}-
{{!}}[[dom/properties/readyState{{!}}'''readyState''']]
{{!}}Retrieves the current state of the object.
{{!}}-
{{!}}[[html/attributes/role{{!}}'''role''']]
{{!}}Sets or retrieves the role for this element.
{{!}}-
{{!}}'''scopeName'''
{{!}}Gets the namespace defined for the element. 

This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/tagUrn{{!}}'''tagUrn''']]
{{!}}Sets or gets the URN specified in the namespace declaration. 

This property is not supported for Metro style apps using JavaScript.
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
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}