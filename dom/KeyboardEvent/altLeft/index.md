{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/KeyboardEvent
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''altLeft''' property to indicate when the user presses the left or right ALT keys.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/starLeft.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function init() {
    spanLeftAlt.innerText{{=}}'false';
    spanRightAlt.innerText{{=}}'false';
}

function indicate(obj, arg) {
    obj.innerText{{=}}arg;
}

function AltDown() {
    if (event.altLeft) {
        indicate(spanLeftAlt,'true');
    }
    else {
        if (event.altKey) {
             indicate(spanRightAlt,'true');
        }
    }
}
    
function AltUp() {
    if (!event.altKey) {
        indicate(spanLeftAlt,'false');
        indicate(spanRightAlt,'false');
    }
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;

&lt;BODY onload{{=}}"document.body.focus(); init()" onkeydown{{=}}"AltDown();" onkeyup{{=}}"AltUp();"&gt;

&lt;P&gt;Press either the left or right ALT key.&lt;/P&gt;
&lt;TABLE&gt;
&lt;TR&gt;
&lt;TD&gt;&lt;I&gt;Left ALT Key Pressed&lt;/I&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;I&gt;Right ALT Key Pressed&lt;/I&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;TR&gt;
&lt;TD ALIGN{{=}}"center"&gt;&lt;SPAN ID{{=}}"spanLeftAlt"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;TD ALIGN{{=}}"center"&gt;&lt;SPAN ID{{=}}"spanRightAlt"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;/P&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property is currently supported only in Microsoft Windows NT 4.0 and Windows 2000.
The [[dom/Document|Document]] must have 
[[dom/methods/focus|'''focus''']]
for this property to return true.
No '''altRight''' property is available. Authors can test for the right ALT key by using the '''altKey''' and '''altLeft''' properties.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>event</code>
*<code>altKey</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}