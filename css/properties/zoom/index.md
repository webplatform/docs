{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Deletion_Candidate
| zoom was originally only supported by Internet Explorer. It is now outdated and shouldn't be recommended any more.
}}
|Checked_Out=No
|High-level issues=Deletion Candidate, Unreviewed Import
|Content=Not Neutral, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Specifies the magnification scale of the object.}}
{{CSS_Selector
|Content====Syntax===
<code>'''zoom: '''normal number percentage</code>

===Remarks===
Setting the value of the <code>zoom</code> property on a rendered object causes the content that surrounds the object to reflow.
Even though the <code>zoom</code> property is not inherited, it affects its children.  This effect is similar to the transformation caused by the [[html/attributes/background (Body element)|'''background''']] and [[css/media queries/filter|'''-ms-filter''']] properties.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''-ms-zoom''' attribute and the '''-ms-zoom''' property to change the magnification scale of a '''p''' element.
|Code=&lt;STYLE&gt;
  .clsTeenyWeeny  { zoom: 0.10 }
&lt;/STYLE&gt;
|LiveURL=This example uses a style rule in an embedded style sheet to set the '''-ms-zoom''' attribute to one-tenth of normal.
}}{{Single Example
|Description=This example uses inline scripting to set the '''-ms-zoom''' property to 200% when an [[dom/events/mouseover|'''onmouseover''']] event occurs.  The magnification scale returns to normal when the [[dom/events/mouseout|'''onmouseout''']] event occurs.
|Code=&lt;P onmouseover{{=}}"this.style.zoom{{=}}'200%'" 
   onmouseout{{=}}"this.style.zoom{{=}}'normal'"&gt;
}}{{Single Example
|Description=This example provides controls that let the user adjust the '''-ms-zoom''' property.
|Code=&lt;html xmlns:control{{=}}""&gt;
&lt;head&gt;
&lt;title&gt;Zoom Demo&lt;/title&gt;
&lt;script type{{=}}"text/javascript"&gt; 
function zoomIn() {
  newZoom{{=}} parseInt(oZoom.style.zoom)+10+'%'
      oZoom.style.zoom {{=}}newZoom;
	  oCode.innerText{{=}}'zoom: '+newZoom+'';	
  } 
function zoomOut() {
  newZoom{{=}} parseInt(oZoom.style.zoom)-10+'%'
      oZoom.style.zoom {{=}}newZoom;
	  oCode.innerText{{=}}'zoom: '+newZoom+'';	
  } 
function changeZoom() {
  newZoom{{=}} parseInt(oSlider.value)
		oZoom.style.zoom{{=}}newZoom+'%';
		oCode.innerText{{=}}'zoom: '+newZoom+'%';	
  } 
function changeZoom2(oSel) {
  newZoom{{=}} oSel.options[oSel.selectedIndex].innerText
		oZoom.style.zoom{{=}}newZoom;
		oCode.innerText{{=}}'zoom: '+newZoom+'';	
  } 
&lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"oZoom.style.zoom{{=}}'100%'; 
    oCode.innerText{{=}}'zoom: 100%'; "&gt;
&lt;!-- Slider and + and - controls  --&gt;
&lt;div style{{=}}"position: absolute; top: 15px; left: 20px;"&gt;
    &lt;form&gt;
&lt;control:slider id{{=}}"oSlider" style{{=}}"sl--orientation:vertical; 
    height:204px; width:28px; background-color:#336699; 
    padding-left:5px; border-left:1px solid #6699CC" tickinterval{{=}}"10"   
    max{{=}}"200" min{{=}}"0" onchange{{=}}"changeZoom()"&gt; &lt;/control:slider&gt;
    &lt;/form&gt;
&lt;/div&gt;
&lt;div style{{=}}"position: absolute; top: 15px; left: 48px; width: 28px; height: 200px; background-color: #336699;" align{{=}}"center"&gt;
    &lt;img src{{=}}"/workshop/graphics/zoomscale.gif" alt{{=}}"scale" border{{=}}"0" usemap{{=}}"#scaler"&gt;
&lt;/div&gt;
&lt;!-- The zoomable area container --&gt;
&lt;div style{{=}}"position: absolute; top: 15px; left: 76px; width: 550px; height: 204px; background-color: black; vertical-align: middle; padding: 25px; font-family: arial; font-weight: bold; color: white; z-index: 3" align{{=}}"center"&gt;
    &lt;!-- The zoomable area --&gt;
    &lt;div id{{=}}"oZoom" style{{=}}"zoom: 100%" align{{=}}"center"&gt;
        &lt;h1&gt;Welcome to Seattle!&lt;/h1&gt;
        &lt;img src{{=}}"/workshop/graphics/seattlesmall.jpg" alt{{=}}"Seattle skyline" align{{=}}"left"&gt;
        &lt;p align{{=}}"center"&gt;A great city in the beautiful state of Washington.&lt;/p&gt;
    &lt;/div&gt;
&lt;/div&gt;
&lt;!-- Displayed code --&gt;
&lt;div style{{=}}"overflow: hidden; border: 1px solid black; position: absolute; top: 219px; left: 20px; width: 606px; height: 90px; padding: 1px; padding-left: 25px; background-color: white; z-index: 3;"&gt;
    &lt;span&gt;&amp;lt;div style{{=}}&amp;quot;&lt;/span&gt;
    &lt;span style{{=}}"font-weight: bold; font-family: verdana; color: red; font-size: 9pt" class{{=}}"coder" id{{=}}"oCode"&gt;
    &lt;/span&gt;&lt;span&gt;&amp;quot;&amp;gt;&lt;/span&gt;
    &lt;div&gt;
        &amp;lt;h1&amp;gt; Welcome to seattle!&amp;lt;/h1&amp;gt;&lt;/div&gt;
    &lt;div&gt;
        &amp;lt;img src{{=}}&amp;quot;seattlesmall.jpg&amp;quot;&amp;gt;&lt;/div&gt;
    &lt;div&gt;
        &amp;lt;p&amp;gt;A great city in the beautiful state of Washington.&amp;lt;/p&amp;gt;&lt;/div&gt;
    &lt;div class{{=}}"coder"&gt;
        &amp;lt;/div&amp;gt;&lt;/div&gt;
&lt;/div&gt;
&lt;div id{{=}}"oControls" style{{=}}"position: absolute; top: 308px; left: 20px; width: 606px; height: 100px; background-color: gray; color: white; font-family: verdana; font-size: 11pt; font-weight: normal; padding: 10px; z-index: 3; text-align: center; border: 1px solid black; text-align: left;"&gt;
    &lt;div style{{=}}"padding-left: 65px"&gt;
        The code used to generate the image is shown in the area above. &lt;br&gt;
        &lt;br&gt;
        Modify the image using the selections below or the &lt;br&gt;
        slider control above and to the left of this window. &lt;/div&gt;
    &lt;hr&gt;
    &lt;div align{{=}}"center"&gt;
        &lt;select id{{=}}"percent" onchange{{=}}"changeZoom2(percent); "&gt;
        &lt;option selected{{=}}""&gt;Use Percentage Value&lt;/option&gt;
        &lt;option&gt;10%&lt;/option&gt;
        &lt;option&gt;25%&lt;/option&gt;
        &lt;option&gt;50%&lt;/option&gt;
        &lt;option&gt;75%&lt;/option&gt;
        &lt;option&gt;100%&lt;/option&gt;
        &lt;option&gt;150%&lt;/option&gt;
        &lt;option&gt;200%&lt;/option&gt;
        &lt;/select&gt; &lt;select id{{=}}"normal" onchange{{=}}"changeZoom2(normal); "&gt;
        &lt;option selected{{=}}""&gt;Use Number Value&lt;/option&gt;
        &lt;option&gt;.1&lt;/option&gt;
        &lt;option&gt;0.25&lt;/option&gt;
        &lt;option&gt;0.5&lt;/option&gt;
        &lt;option&gt;0.75&lt;/option&gt;
        &lt;option&gt;1.0&lt;/option&gt;
        &lt;option&gt;1.5&lt;/option&gt;
        &lt;option&gt;2.0&lt;/option&gt;
        &lt;/select&gt;&lt;hr&gt;&lt;/div&gt;
&lt;/div&gt;
&lt;map name{{=}}"scaler"&gt;
&lt;area shape{{=}}"rect" coords{{=}}"0,182,19,199" alt{{=}}"plus" href{{=}}"#" onclick{{=}}"zoomIn()" style{{=}}"cursor: hand"&gt;
&lt;area shape{{=}}"rect" coords{{=}}"1,1,18,15" alt{{=}}"minus" href{{=}}"#" onclick{{=}}"zoomOut()"&gt;
&lt;/map&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/zoom.htm
}}
}}
{{Notes_Section}}
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
|Topic_clusters=Visual Effects
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}