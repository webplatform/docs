{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Fires when the user moves the mouse over the object.}}
{{Event
|Event_applies_to=dom/MouseEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=No
|Default_action=none
|Interface=dom/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onmousemove''' event to monitor the location of the mouse cursor on the screen. When the mouse cursor moves over the '''div''' object, a '''span''' object is updated with the [[dom/MouseEvent/clientX|'''clientX''']] and [[dom/MouseEvent/clientY|'''clientY''']] property values. The '''clientX''' and '''clientY''' properties are exposed by the event object.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnTrackMouse(){
   oNotice.innerText{{=}}"Coords: (" + event.clientX + ", 
      " + event.clientY + ")";
}
&lt;/script&gt;
&lt;div id{{=}}"oScratch" onmousemove{{=}}"fnTrackMouse()"&gt;
  &lt;span id{{=}}"oNotice"&gt;&lt;/span&gt;
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousemoveEX.htm
}}{{Single Example
|Language=JavaScript
|Description=Add mouse crosshairs to a web page when a checkbox is clicked.
|Code=function moveCrosshairs(evt){
         if(!evt)evt=window.event;       
         var posx = 0; var posy = 0; 
         if(document.documentMode&&document.documentMode>=9){ 
         posx+=parseInt(document.documentElement.style.marginLeft+0); 
         posy+=parseInt(document.documentElement.style.marginTop+0); 
         } 
         if (evt.pageX || evt.pageY)  {  
         	posx += evt.pageX - document.documentElement.scrollLeft - document.body.scrollLeft;
         	posy += evt.pageY - document.documentElement.scrollTop - document.body.scrollTop;
          } 
        else if (evt.clientX || evt.clientY)  { 
        	posx += evt.clientX;  
        	posy += evt.clientY; 
        } 
           	dX=document.getElementById('divX'); 
           	dX.style.left=(10+posx+'px'); 
	   		dY=document.getElementById('divY'); 
	   		dY.style.top=(10+posy+'px');    
		}
		function toggleCrosshairs(evt){
        if(!evt)evt=window.event;    
        var el=('target' in evt)?evt.target:evt.srcElement;    
        if(el.checked){     
        	if(window.addEventListener)     {
        		window.addEventListener('mousemove',moveCrosshairs,true);
        	}     else     {
        		document.documentElement.attachEvent('onmousemove',moveCrosshairs);
        	}    
        }else{     
        if(window.removeEventListener)     {
        	window.removeEventListener('mousemove', moveCrosshairs,true);     
        	document.getElementById('divX').style.left='-10px';     
        	document.getElementById('divY').style.top='-10px';     
        }     
        else     {
        	document.documentElement.detachEvent('onmousemove', moveCrosshairs);
        	document.getElementById('divX').style.left='-10px';
        	document.getElementById('divY').style.top='-10px';
        }   
		}
		}
|LiveURL=http://result.dabblet.com/gist/7c3297a000687b42de03/011b604311ed518c148e9d88637ae79f32e7a4f7
}}
}}
{{Notes_Section
|Notes====Remarks===
If the user presses a mouse button, use the '''button''' property to determine which button was pressed.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse over the document.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/mousemove mousemove event]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536947(v=vs.85).aspx mousemove event]
|HTML5Rocks_link=
}}