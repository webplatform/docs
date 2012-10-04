{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to retrieve a collection of '''input type{{=}}text''', '''div''' and '''button'''. The '''children''' collection for <code>oChildDIV</code> includes '''p'''.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/children.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
...
&lt;SCRIPT&gt;
var oColl; //Collection for children.
var oRow, oCell; //Use for row and cell.
function fnCollection(){
    oColl {{=}} oParentDIV.children;
	//Call function to create cells for the top parent object.
	getChildren(oColl, oParentDIV);
	/*Call function to create cells for the child within the parent object
        containing its own child.*/
	oColl {{=}} oChildDIV.children;
	getChildren(oColl, oChildDIV);
}
/*****************************************************************************
In:
	oColl - Collection of children.
	oCollection - Parent object.
Out: 
	Output to screen.
******************************************************************************/
function getChildren(oColl, oCollection){
	for(x{{=}}0;x&lt;oColl.length;x++){
	        //Create new row.
        	oRow {{=}} oTable.insertRow();
        
	        //Create cell with the array index of current child.
        	oCell {{=}} oRow.insertCell();
	        oCell.align {{=}} 'center';
        	oCell.style.color {{=}} '#0000FF';
	        oCell.innerText {{=}} x;
	
        	//Create cell with the tagName of current child.          
	        oCell {{=}} oRow.insertCell();
        	oCell.align {{=}} 'center';
	        oCell.innerText {{=}} oCollection.children.item(x).tagName;
	        //Create cell with ID / name of current child.            
	        oCell {{=}} oRow.insertCell();
        	oCell.align {{=}} 'center';
	        if(oCollection.children.item(x).name !{{=}} null){
        	    oCell.innerText {{=}} oCollection.children.item(x).name;
	        }else{
        	    oCell.innerText {{=}} oCollection.children.item(x).id;
	        }
		
		//Create cell with applicable Parent object to the child.
		oCell {{=}} oRow.insertCell();
		oCell.align {{=}} 'center';
		oCell.innerText {{=}} oCollection.id;
	}
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;CENTER&gt;
&lt;SPAN class{{=}}"oTitle"&gt;DIV Object (ID: oParentDIV)&lt;/SPAN&gt;
&lt;DIV id{{=}}"oParentDIV" class{{=}}"oDIV"&gt;
	Some Input (non-editable): &lt;INPUT type{{=}}"text" name{{=}}"SomeInputTextBox"
        value{{=}}"" size{{=}}"5"  CONTENTEDITABLE{{=}}"false"&gt;
  &lt;DIV id{{=}}"oChildDIV"&gt;
    &lt;P id{{=}}"oParagraph1"&gt;Some text in a paragraph&lt;/P&gt;
  &lt;/DIV&gt;
  &lt;BUTTON name{{=}}"SomeButton" onclick{{=}}"alert('Some alert.');"&gt;The Label for
        the Button&lt;/BUTTON&gt;
&lt;/DIV&gt;
&lt;HR&gt;
&lt;BUTTON id{{=}}"b1" onclick{{=}}"fnCollection(); b1.disabled{{=}}true;"
    style{{=}}"cursor:hand"&gt;Retrieve Collection&lt;/BUTTON&gt;
&lt;BR&gt;&lt;BR&gt;
&lt;TABLE border{{=}}"1" id{{=}}"oTable" alt{{=}}"Child Listing"&gt;
&lt;TR&gt;
    &lt;TH&gt;Array Index&lt;/TH&gt;&lt;TH&gt;Child Element&lt;/TH&gt;&lt;TH&gt;ID&lt;/TH&gt;&lt;TH&gt;Parent Object&lt;/TH&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/CENTER&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Similar to the objects contained in the [[dom/properties/all|'''all''']] collection, the objects contained in the '''children''' collection are undefined if the child elements are overlapping tags.
The '''children''' collection can contain HTML elements.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}