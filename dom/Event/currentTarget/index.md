{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/Event
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The [[dom/properties/target|'''target''']] property returns the element that originally received an event. However, the '''currentTarget''' property returns the element that the event handlers are being processed for during the capturing and bubbling phases. At event phase <code>AT_TARGET</code>, the '''currentTarget''' and '''target''' objects are the same object.
In 
Windows Internet Explorer 8 and earlier versions, the '''event''' object does not provide access to the current event target. For the equivalent functionality, specify the <code>this</code> keyword as an argument to the event handler, as the following code example shows.
 <code>&lt;button id{{=}}"target" onclick{{=}}"myHandler(event, this);"&gt;...&lt;/button&gt;
 function myHandler(evt, elem) {
     alert(elem.id);
 } </code>
Alternatively, if the event handler is set with an event property, the current target is set as the <code>this</code> keyword when the event handler is invoked, as the following code example shows.
 <code>document.getElementById('target').onclick {{=}} myHandler;
 function myHandler(evt) {
     alert(this.id);
 } </code>
If you use [[dom/methods/attachEvent|'''attachEvent''']], you cannot access the current event target in the event handler.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/objects/SVGZoom|SVGZoomEvent]]</code>
*<code>[[dom/objects/BeforeUnloadEvent|BeforeUnloadEvent]]</code>
*<code>[[dom/objects/CompositionEvent|CompositionEvent]]</code>
*<code>[[dom/objects/CustomEvent|CustomEvent]]</code>
*<code>[[dom/objects/Event|Event]]</code>
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/FocusEvent|FocusEvent]]</code>
*<code>[[dom/objects/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/objects/MessageEvent|MessageEvent]]</code>
*<code>[[dom/objects/MouseEvent|MouseEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/MutationEvent|MutationEvent]]</code>
*<code>[[dom/objects/MSSiteModeEvent|MSSiteModeEvent]]</code>
*<code>[[dom/objects/StorageEvent|StorageEvent]]</code>
*<code>[[dom/objects/TextEvent|TextEvent]]</code>
*<code>[[dom/objects/UIEvent|UIEvent]]</code>
*<code>[[dom/properties/eventPhase|eventPhase]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}