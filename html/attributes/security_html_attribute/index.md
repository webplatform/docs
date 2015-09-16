---
title: 'security html attribute'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/securityEX.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/security2.htm'
compatibility:
  feature: 'security html attribute'
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/createElement
uri: 'html/attributes/security html attribute'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

The following example shows how to give the user the choice of loading a document into a restricted or unrestricted **iframe**. Note that the [**createElement**](/w/index.php?title=dom/methods/createElement&action=edit&redlink=1) method is used to create the two frames. The **createElement** method must use an HTML string for the parameter to specify the **SECURITY** attribute dynamically; after the **iframe** is parsed into the document, it cannot be altered.

``` html
<HTML>
<HEAD>
<SCRIPT>
var bRestShown = false;
var bUnRestShown = false;
function createIframe(){
    var sContents;
    if (event.srcElement.id=="restricted" && bRestShown!=true){
        sContents = "<IFRAME SECURITY='restricted' SRC='frameSource.htm'>"
        var newIframe = document.createElement(sContents);
        restIframe.appendChild(newIframe);}
   else if (event.srcElement.id=="unrestricted" && bUnRestShown!=true){
        sContents = "<IFRAME SRC='frameSource.htm'>"
        var newIframe = document.createElement(sContents);
        unRestIframe.appendChild(newIframe);}

}
</SCRIPT>
</HEAD>
<BODY>
<table>
<TR>
<TD><INPUT ID="restricted" TYPE="BUTTON" ONCLICK="createIframe();bRestShown=true;"
VALUE="Create Restricted IFRAME"></TD>
<TD><INPUT ID="unrestricted" TYPE="BUTTON" ONCLICK="createIframe();bUnRestShown=true;" VALUE="Create Unrestricted IFRAME"></TD>
</TR>
<tr>
<td>
<b>IFRAME with SECURITY="restricted"</b>
</td>
<td>
<b>IFRAME without SECURITY attribute</b>
</td>
</tr>
<TR>
<td>
<SPAN id="restIframe"></SPAN>
</td>
<td>
<SPAN id="unRestIframe"></SPAN>
</td>
</tr>
</table>
<BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/securityEX.htm)

Hyperlinks that are clicked and forms that are submitted in the restricted frame open in a new window. If the page contains script, it can be executed at that time, depending on the security settings of the zone. The following example demonstrates how to disable hyperlinks and submit buttons that might compromise security. Note: The embedded page must be in the same domain.

``` html
<HTML>
<HEAD>
<TITLE>Restricted IFRAME - Hosting Script</TITLE>
</HEAD>
<BODY>
<H1>Restricted IFRAME</H1>
<P>The page below cannot run script, but try clicking the link.</P>
<iframe name="myFrame" width="50%" height="200" src="security2_script.htm" security="restricted"></iframe>
<br><button id="btnDisable" onclick="disableAll()">Disable Links and Buttons</button>
<script type="text/javascript" language="jscript">
function disableAll()
{
    var doc = document.frames("myFrame").document;

    disableLinks(doc.links);

    disableSubmitButtons(doc.getElementsByTagName("INPUT"));
    disableSubmitButtons(doc.getElementsByTagName("BUTTON"));

    btnDisable.disabled = true;
}
function disableLinks(c)
{
    for (var i=0; i<c.length; i++)
    {
        // display the href as a ToolTip
        c[i].title = c[i].href;
        c[i].href = "about:blank";
        c[i].disabled = true;
    }
}
function disableSubmitButtons(c)
{
    for (var i=0; i<c.length; i++)
    {
        if (c[i].type == "submit")
            c[i].disabled = true;
    }
}
</script>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/security2.htm)

## Notes

### Remarks

The *sSecure* value must specify `restricted`. Because **SECURITY** is an attribute only, it must be defined in the **frame** element declaration. If a frame is restricted by the **SECURITY** attribute, all nested frames share the same restrictions. The **SECURITY** attribute applies the user security setting *Restricted Sites* to the source file of a **frame** or **iframe**. (Zone settings are found on the **Security** tab of the **Internet Options** dialog box.) By default, scripting is not enabled in the Restricted Sites zone. By changing the security settings of the zone, various negative results can occur, including, but are not limited to, allowing script to run. Independent of user security settings, the **SECURITY** attribute affects the behavior of hyperlinks and forms inside a restricted **frame** or **iframe** in the following two ways.

-   Hyperlinks and forms open in a new window. This happens even when the [**TARGET**](/html/attributes/target) attribute specifies `"_self"` for a frame nested in the restricted frame. In the following example, when you click a hyperlink in the **iframe**, a new window opens with the requested document.

        <code><IFRAME SECURITY{{=}}"restricted" src{{=}}"http://www.microsoft.com"></IFRAME></code>

    -   The **SECURITY** attribute restricts use of the **frame** or **iframe**, the source file cannot execute the following code.

        <code><A HREF{{=}}"javascript:alert('Disallowed in restricted FRAME or IFRAME!');">JavaScript Link</A></code>

    **Security Warning:  ** If the restricted document contains script, the script can be executed when the page is opened in a new window, depending on the security settings of the zone. This is not a problem if the restricted **iframe** contains inline content, for example, there is no [**src**](/html/attributes/src_(iframe,_embed,_xml)) attribute; or if the content comes from a another more restricted domain, for example, contoso.com hosts a page from untrusted.com. However, when content from the same domain is hosted in a restricted frame, care should be taken to limit the action of hyperlinks and forms. Refer to the following example. You can access the properties and contents of a restricted **frame** or **iframe** through the Document Object Model (DOM) of the container document. **SECURITY** was introduced in Microsoft Internet Explorer 6

    ### Syntax

    ### Standards information

    There are no standards that apply here.

    ### Requirements

    {

    ## See also

    ### Related pages

    -   `frame`
    -   `iframe`
