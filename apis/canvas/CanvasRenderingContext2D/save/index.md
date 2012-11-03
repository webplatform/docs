{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Saves the current state of the context. Use the restore() method to retrieve the saved state.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''save''' and [[canvas/methods/restore|'''restore''']] methods  preserve and restore the state of a context, but not specific paths or graphics. The following attributes and states are affected:
*The current transformation matrix
*The current clipping region
*The current values of the following attributes:
<table class{{=}}"clsStd">
<tr>
<th>Attribute</th>
<th/>
</tr>
<tr>
<td>

</td>
<td>

</td>
</tr>
</table>
 
**[[canvas/properties/strokeStyle|'''strokeStyle''']]
**[[canvas/properties/fillStyle|'''fillStyle''']]
**[[canvas/properties/globalAlpha|'''globalAlpha''']]
**[[canvas/properties/lineWidth|'''lineWidth''']]
**[[canvas/properties/lineCap|'''lineCap''']]
**[[canvas/properties/lineJoin|'''lineJoin''']]
**[[canvas/properties/miterLimit|'''miterLimit''']]
|Import_Notes====Standards information===
*[http://www.w3.org/TR/2dcontext/ HTML Canvas 2D Context]

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
|Manual_links=*<code>[[canvas/methods/restore|restore]]</code>
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*[[/tutorials/canvas/Canvas_tutorial/Transformations|Transformations]]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}