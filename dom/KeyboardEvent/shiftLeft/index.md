{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/KeyboardEvent
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''shiftLeft''' property to indicate when the user presses the left or right SHIFT keys.
|Code=&lt;HEAD&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[dom/Document|Document]] must have 
[[dom/HTMLElement/focus|'''focus''']]
for this property to return true.
|Import_Notes====Syntax===
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}