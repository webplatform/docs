{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example declares  the '''SVGLengthList''' object as read-only and identifies the appropriate exceptions to raise.
|LiveURL=
|Code=
 
interface SVGLengthList {
  readonly attribute unsigned long numberOfItems;
  void clear() raises(DOMException);
  SVGLength initialize(in SVGLength newItem) raises(DOMException);
  SVGLength getItem(in unsigned long index) raises(DOMException);
  SVGLength insertItemBefore(in SVGLength newItem, in unsigned long index) raises(DOMException);
  SVGLength replaceItem(in SVGLength newItem, in unsigned long index) raises(DOMException);
  SVGLength removeItem(in unsigned long index) raises(DOMException);
  SVGLength appendItem(in SVGLength newItem) raises(DOMException);
};
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
You can designate an '''SVGLengthList''' object as read-only, so that any attempts to modify the object  cause a <code>NoModificationAllowedError</code> exception that is defined  during initialization.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.13


===Members===
The '''SVGLengthList''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''SVGLengthList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/appendItem|'''appendItem''']]
|Inserts a new item at the end of the list.
|-
|[[svg/methods/clear|'''clear''']]
|Clears all existing items from the list, which creates  an empty list.
|-
|[[svg/methods/getItem|'''getItem''']]
|Returns the specified item from a list.
|-
|[[svg/methods/initialize|'''initialize''']]
|Clears current items from the list and re-initializes the list to  contain  the  specified item.
|-
|[[svg/methods/insertItemBefore|'''insertItemBefore''']]
|Inserts a new item into a list at a specified position.
|-
|[[svg/methods/removeItem|'''removeItem''']]
|Removes an existing item from the list.
|-
|[[svg/methods/replaceItem|'''replaceItem''']]
|Replaces a specified  existing item in the list with a specified new item.
|}
 

====Properties====
The '''SVGLengthList''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/numberOfItems|'''numberOfItems''']]
|Gets or sets  the number of items in a list.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}