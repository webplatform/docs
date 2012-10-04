{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLIFrameElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''contentWindow''' property to change the URL of window objects contained inside several '''iframe''' objects.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentWindowEX1.htm
|Code=

&lt;html&gt;
&lt;head&gt;
&lt;SCRIPT&gt;
function fnNavigate()
{
    for(i{{=}}0;i&lt;document.all.length;i++)
    {
        if(document.all(i).tagName{{=}}{{=}}"IFRAME")
        {
            document.all(i).contentWindow.location {{=}} "http://www.msn.com";
        }
    }	
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;BUTTON onclick{{=}}"fnNavigate();"&gt;Navigate Frames&lt;/BUTTON&gt;
&lt;P/&gt;
&lt;IFRAME SRC{{=}}"http://www.microsoft.com" STYLE{{=}}"width:100%;height:150px;"&gt;
&lt;/IFRAME&gt;
&lt;P/&gt;
&lt;IFRAME SRC{{=}}"http://www.microsoft.com" STYLE{{=}}"width:100%;height:150px;"&gt;
&lt;/IFRAME&gt;
&lt;P/&gt;
&lt;IFRAME SRC{{=}}"http://www.microsoft.com" STYLE{{=}}"width:100%;height:150px;"/&gt;
&lt;/IFRAME&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;	

}}}}
{{Notes_Section
|Notes=
===Remarks===
This property is useful if you do not know the [[html/attributes/id|'''id''']] of the '''frame''' or '''iframe''' you are accessing through a collection.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
*<code>[[dom/properties/frameElement|frameElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}