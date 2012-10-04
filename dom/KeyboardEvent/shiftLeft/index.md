{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/KeyboardEvent
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''shiftLeft''' property to indicate when the user presses the left or right SHIFT keys.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function init() {
    spanLeftShift.innerText{{=}}'false';
    spanRightShift.innerText{{=}}'false';
}

function indicate(obj, arg) {
    obj.innerText{{=}}arg;
}

function ShiftDown() {
    if (event.shiftLeft) {
        indicate(spanLeftShift,'true');
    }
    else {
        if (event.shiftKey) {
        indicate(spanRightShift,'true');
        }
    }
}    

function ShiftUp() {
    if (!event.shiftKey) {
        indicate(spanLeftShift,'false');
        indicate(spanRightShift,'false');
    }
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;

&lt;BODY onload{{=}}"document.body.focus(); init()" onkeydown{{=}}"ShiftDown();" onkeyup{{=}}"ShiftUp();"&gt;

&lt;P&gt;Press either the left or right SHIFT key.&lt;/P&gt;
&lt;TABLE&gt;
&lt;TR&gt;
&lt;TD&gt;&lt;I&gt;Left SHIFT Key Pressed&lt;/I&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;I&gt;Right SHIFT Key Pressed&lt;/I&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;TR&gt;
&lt;TD ALIGN{{=}}"center"&gt;&lt;SPAN ID{{=}}"spanLeftShift"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;TD ALIGN{{=}}"center"&gt;&lt;SPAN ID{{=}}"spanRightShift"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/P&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The [[dom/document|'''document''']] must have 
[[dom/methods/focus|'''focus''']]
for this property to return true.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>event</code>
*<code>shiftKey</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}