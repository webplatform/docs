{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the number of times a sound or video clip will loop when activated.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''loop''' property and the [[html/attributes/src|'''src''']] property to change the number of times a background sound loops.
|Code=&lt;SCRIPT&gt;
function loopOnce() {
    oBGSound.loop {{=}} 1;
    oBGSound.src {{=}} oBGSound.src; // reload sound
}
function loopContinuously() {
    oBGSound.loop {{=}} -1;
    oBGSound.src {{=}} oBGSound.src; // reload sound
}
&lt;/SCRIPT&gt;
:
&lt;BGSOUND id{{=}}"oBGSound" src{{=}}"sound.wav"&gt;
&lt;BUTTON onclick{{=}}"loopOnce()"&gt;Loop Sound Once&lt;/BUTTON&gt; 
&lt;BUTTON onclick{{=}}"loopContinuously()"&gt;Loop Sound Continuously&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/loop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
To restart a sound or video clip after changing its '''loop''' property, set the [[html/attributes/src|'''src''']] property or '''dynsrc''' property to itself. For example:
 <code>oBGSound.src {{=}} oBGSound.src</code>
The following are descriptions of how the '''loop''' property works for some boundary cases.
{| class="wikitable"
|-
|&lt;BGSOUND src{{=}}"file:///c:\win95\system\msremind.wav"&gt;
|Loops one time
|-
|&lt;BGSOUND src{{=}}"file:///c:\win95\system\msremind.wav" LOOP&gt;
|Loops one time.
|-
|&lt;BGSOUND src{{=}}"file:///c:\win95\system\msremind.wav" LOOP{{=}}&gt;
|Loops one time.
|-
|&lt;BGSOUND src{{=}}"file:///c:\win95\system\msremind.wav" LOOP{{=}}0&gt;
|Loops one time.
|-
|&lt;BGSOUND src{{=}}"file:///c:\win95\system\msremind.wav" LOOP{{=}}-1&gt;
|Loops infinitely.
|}
 
In Microsoft Internet Explorer 4.0, when you restart a video by changing its '''loop''' property, the video opens and plays in a new window.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>bgSound</code>
*<code>img</code>
*<code>input</code>
*<code>input type{{=}}image</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}