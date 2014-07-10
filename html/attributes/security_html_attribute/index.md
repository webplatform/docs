{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to give the user the choice of loading a document into a restricted or unrestricted '''iframe'''. Note that the [[dom/methods/createElement|'''createElement''']] method is used to create the two frames. The '''createElement''' method must use an HTML string for the parameter to specify the '''SECURITY''' attribute dynamically; after the '''iframe''' is parsed into the document, it cannot be altered.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var bRestShown {{=}} false;
var bUnRestShown {{=}} false;
function createIframe(){
    var sContents;
    if (event.srcElement.id{{=}}{{=}}"restricted" &amp;&amp; bRestShown!{{=}}true){
        sContents {{=}} "&lt;IFRAME SECURITY{{=}}'restricted' SRC{{=}}'frameSource.htm'&gt;"
        var newIframe {{=}} document.createElement(sContents);
        restIframe.appendChild(newIframe);}
   else if (event.srcElement.id{{=}}{{=}}"unrestricted" &amp;&amp; bUnRestShown!{{=}}true){
        sContents {{=}} "&lt;IFRAME SRC{{=}}'frameSource.htm'&gt;"
        var newIframe {{=}} document.createElement(sContents);
        unRestIframe.appendChild(newIframe);}
        
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;table&gt;
&lt;TR&gt;
&lt;TD&gt;&lt;INPUT ID{{=}}"restricted" TYPE{{=}}"BUTTON" ONCLICK{{=}}"createIframe();bRestShown{{=}}true;" 
VALUE{{=}}"Create Restricted IFRAME"&gt;&lt;/TD&gt;
&lt;TD&gt;&lt;INPUT ID{{=}}"unrestricted" TYPE{{=}}"BUTTON" ONCLICK{{=}}"createIframe();bUnRestShown{{=}}true;" VALUE{{=}}"Create Unrestricted IFRAME"&gt;&lt;/TD&gt;
&lt;/TR&gt;
&lt;tr&gt;
&lt;td&gt;
&lt;b&gt;IFRAME with SECURITY{{=}}"restricted"&lt;/b&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;b&gt;IFRAME without SECURITY attribute&lt;/b&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;TR&gt;
&lt;td&gt;
&lt;SPAN id{{=}}"restIframe"&gt;&lt;/SPAN&gt;
&lt;/td&gt;
&lt;td&gt;
&lt;SPAN id{{=}}"unRestIframe"&gt;&lt;/SPAN&gt;
&lt;/td&gt;
&lt;/tr&gt;
&lt;/table&gt;
&lt;BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/securityEX.htm
}}{{Single Example
|Description=Hyperlinks that are clicked and forms that are submitted in the restricted frame open in a new window. If the page contains script, it can be executed at that time, depending on the security settings of the zone. The following example demonstrates how to disable hyperlinks and submit buttons that might compromise security. Note: The embedded page must be in the same domain.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;Restricted IFRAME - Hosting Script&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;H1&gt;Restricted IFRAME&lt;/H1&gt;
&lt;P&gt;The page below cannot run script, but try clicking the link.&lt;/P&gt;
&lt;iframe name{{=}}"myFrame" width{{=}}"50%" height{{=}}"200" src{{=}}"security2_script.htm" security{{=}}"restricted"&gt;&lt;/iframe&gt;
&lt;br&gt;&lt;button id{{=}}"btnDisable" onclick{{=}}"disableAll()"&gt;Disable Links and Buttons&lt;/button&gt;
&lt;script type{{=}}"text/javascript" language{{=}}"jscript"&gt;
function disableAll()
{
    var doc {{=}} document.frames("myFrame").document;
    
    disableLinks(doc.links);
    
    disableSubmitButtons(doc.getElementsByTagName("INPUT"));
    disableSubmitButtons(doc.getElementsByTagName("BUTTON"));
    
    btnDisable.disabled {{=}} true;
}
function disableLinks(c)
{
    for (var i{{=}}0; i&lt;c.length; i++)
    {
        // display the href as a ToolTip
        c[i].title {{=}} c[i].href;
        c[i].href {{=}} "about:blank";
        c[i].disabled {{=}} true;
    }
}
function disableSubmitButtons(c)
{
    for (var i{{=}}0; i&lt;c.length; i++)
    {
        if (c[i].type {{=}}{{=}} "submit")
            c[i].disabled {{=}} true;
    }
}
&lt;/script&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/security2.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The ''sSecure'' value must specify <code>restricted</code>. Because '''SECURITY''' is an attribute only, it must be defined in the '''frame''' element declaration.
If a frame is restricted by the '''SECURITY''' attribute, all nested frames share the same restrictions.
The '''SECURITY''' attribute applies the user security setting ''Restricted Sites'' to the source file of a '''frame''' or '''iframe'''. (Zone settings are found on the '''Security''' tab of the '''Internet Options''' dialog box.) By default, scripting is not enabled in the Restricted Sites zone. By changing the security settings of the zone, various negative results can occur, including, but are not limited to, allowing script to run.
Independent of user security settings, the '''SECURITY''' attribute affects the behavior of hyperlinks and forms inside a restricted '''frame''' or '''iframe''' in the following two ways.
*Hyperlinks and forms open in a new window. This happens even when the [[html/attributes/target|'''TARGET''']] attribute specifies <code>"_self"</code> for a frame nested in the restricted frame. In the following example, when you click a hyperlink in the '''iframe''', a new window opens with the requested document. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>&lt;IFRAME SECURITY{{=}}"restricted" src{{=}}"http://www.microsoft.com"&gt;&lt;/IFRAME&gt;</code></pre>
</div>
*The '''SECURITY''' attribute restricts use of the '''frame''' or '''iframe''', the source file cannot execute the following code. 
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>&lt;A HREF{{=}}"javascript:alert('Disallowed in restricted FRAME or IFRAME!');"&gt;JavaScript Link&lt;/A&gt;</code></pre>
</div>

'''Security Warning:  ''' If the restricted document contains script, the script can be executed when the page is opened in a new window, depending on the security settings of the zone. This is not a problem if the restricted '''iframe''' contains inline content, for example, there is no [[html/attributes/src (iframe, embed, xml)|'''src''']] attribute; or if the content comes from a another more restricted domain, for example, contoso.com hosts a page from untrusted.com. However, when content from the same domain is hosted in a restricted frame, care should be taken to limit the action of hyperlinks and forms. Refer to the following example.
You can access the properties and contents of a restricted '''frame''' or '''iframe''' through the Document Object Model (DOM) of the container document.
'''SECURITY''' was introduced in Microsoft Internet Explorer 6
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows 2000 Server
|}
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
*<code>frame</code>
*<code>iframe</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}