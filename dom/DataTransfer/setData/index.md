{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=format|Data type=BSTR|Description=A '''String''' that specifies the format of the data to be transferred, using one of the following values.|Optional=}}
{{Method Parameter|Name=data|Data type=VARIANT|Description=A '''Variant''' of type '''String''' that specifies the data supplied by the source object. This information can be descriptive text, a source path to an image, or a URL for an anchor. When you pass "URL" as the ''format'' parameter, you must use the ''data'' parameter to provide the location of the object that is transferred.|Optional=}}
|Method_applies_to=dom/clipboardData,dom/properties/dataTransfer
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

'''Boolean'''. Returns one of the following possible values.

{| class="wikitable"
|-
!Return value
!Description
|-
|true
|The data was successfully added.
|-
|false
|The data was not added.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''setData''' method and the [[dom/methods/getData|'''getData''']] method with the [[dom/objects/dataTransfer|'''dataTransfer''']] object to create a shortcut to an image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setDataEX.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var sImageURL;
function InitiateDrag() 
/*  The setData parameters tell the source object
   to transfer data as a URL and provide the path.  */
{   
    event.dataTransfer.setData("URL", oImage.src);
}
function FinishDrag()
/*  The parameter passed to getData tells the target
    object what data format to expect.  */
{
    sImageURL {{=}} event.dataTransfer.getData("URL")
    oTarget.innerText {{=}} sImageURL;
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P&gt;This example demonstrates how to use the setData and
   getData methods of the dataTransfer object to enable the
   source path of the image to be dragged.&lt;/P&gt;
&lt;IMAGE ID{{=}}oImage SRC{{=}}"/workshop/graphics/black.png" 
       ondragstart{{=}}"InitiateDrag()"&gt;
&lt;SPAN ID{{=}}oTarget ondragenter{{=}}"FinishDrag()"&gt;
    Drop the image here
&lt;/SPAN&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The value of the ''format'' parameter is not case-sensitive.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/clipboardData|clipboardData]]</code>
*<code>[[dom/objects/dataTransfer|dataTransfer]]</code>
*<code>Reference</code>
*<code>[[dom/methods/clearData|clearData]]</code>
*<code>[[dom/methods/getData|getData]]</code>
*<code>Conceptual</code>
*<code>About DHTML Data Transfer</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}