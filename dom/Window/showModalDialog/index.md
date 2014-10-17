{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up MSDN import, move IE-specific content to compatibility
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Do not use. Use <dialog> or a popup window instead. Halts the script execution, creates a popup window, passes it parameters and returns a value when the new window is closed.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=url
|Data type=String
|Description='''String''' that specifies the URL of the document to load and display.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=argumentsToPass
|Data type=any
|Description=The arguments to use when displaying the new document. Use this parameter to pass a value of any type, including an array of values. The dialog box can extract the values passed by the caller from the [[dom/WindowModal/dialogArguments|'''dialogArguments''']] property.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=windowOptions
|Data type=String
|Description=Specifies the window ornaments for the dialog box, using one or more of the following semicolon-delimited values:
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Return_value_name=returnValue
|Javascript_data_type=any
|Return_value_description=The value of the '''returnValue''' property as set by the window of the document specified in ''url''.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''showModalDialog''' method to open a customized dialog box.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnRandom(iModifier){
   return parseInt(Math.random()*iModifier);
}
function fnSetValues(){
   var iHeight{{=}}oForm.oHeight.options[
      oForm.oHeight.selectedIndex].text;
   if(iHeight.indexOf("Random")&gt;-1){
      iHeight{{=}}fnRandom(document.body.clientHeight);
   }
   var sFeatures{{=}}"dialogHeight: " + iHeight + "px;";
   return sFeatures;
}
function fnOpen(){
   var sFeatures{{=}}fnSetValues();
   window.showModalDialog("showModalDialog_target.htm", "", 
      sFeatures)
}
&lt;/script&gt;
&lt;form name{{=}}"oForm"&gt;
	Dialog Height 
  &lt;select name{{=}}"oHeight"&gt;
    &lt;option&gt;-- Random --&lt;/option&gt;
    &lt;option&gt;150&lt;/option&gt;
    &lt;option&gt;200&lt;/option&gt;
    &lt;option&gt;250&lt;/option&gt;
    &lt;option&gt;300&lt;/option&gt;
  &lt;/select&gt; 
	Create Modal Dialog Box
  &lt;input type{{=}}"button" value{{=}}"Push To Create" onclick{{=}}"fnOpen()"&gt;
&lt;/form&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/showModalDialog2.htm
}}
}}
{{Notes_Section
|Usage=Do not use. This API is being phased out. Chrome and Opera have already removed it by default and Firefox also considers following suit.
|Notes=A modal dialog box retains the input focus while open. The user cannot switch windows until the dialog box is closed.
Because a modal dialog box can include a URL to a resource in a different domain, do not pass information through the ''varArgIn'' parameter that the user might consider private. The ''varArgIn'' parameter can be referenced within the modal dialog box using the [[dom/WindowModal/dialogArguments|'''dialogArguments''']] property of the '''window''' object. If the ''varArgIn'' parameter is defined as a string, the maximum string length that can be passed to the modal dialog box is 4096 characters; longer strings are truncated.
You can set the default font settings the same way you set Cascading Style Sheets (CSS) attributes (for example, <code>"font:3;font-size:4"</code>). To define multiple font values, use multiple font attributes.
To override <code>center</code>, even though the default for <code>center</code> is <code>yes</code>, you can specify either <code>dialogLeft</code> and/or <code>dialogTop</code>.
When Windows Internet Explorer opens a window from a modal or modeless HTML dialog box by using the '''showModalDialog''' method or by using the [[dom/HTMLElement/showModelessDialog|'''showModelessDialog''']] method, Internet Explorer uses Component Object Model (COM) to create a new instance of the window. Typically, the window is opened by using the first instance of an existing Internet Explorer process. When Internet Explorer opens the window in a new process, all the memory cookies are no longer available, including the session ID. This process is different from the process that Windows Internet Explorer uses to open a new window by using the [[dom/Window/open|'''open''']] method.
For Windows Internet Explorer 7, <code>dialogHeight</code> and <code>dialogWidth</code> return the height and width of the content area and no longer includes the height and width of the frame.
Internet Explorer 7.  Although a user can manually adjust the height of a dialog box to a smaller value —provided the dialog box is resizable— the minimum <code>dialogHeight</code> you can specify is 100 pixels, and the minimum <code>dialogWidth</code> you can define is 250 pixels. In versions earlier than Internet Explorer 7 the minimum value of the <code>dialogWidth</code> that can be specified is 100 pixels.

'''Note'''  For Internet Explorer 7, <code>help</code> is not a valid value for <code>sFeatures</code>. In previous versions, <code>help:{ yes {{!}} no {{!}} 1 {{!}} 0 {{!}} on {{!}} off }</code> specified whether the dialog window displays the context-sensitive Help icon.
This method must use a user-initiated action, such as clicking on a link or tabbing to a link and pressing enter, to open a pop-up window. The Pop-up Blocker feature in Microsoft Internet Explorer 6 blocks windows that are opened without being initiated by the user.
Microsoft Internet Explorer 5 and later  allows further control over modal dialog boxes through the <code>status</code> and <code>resizable</code> values in the ''varOptions'' parameter of the '''showModalDialog''' method. Turn off the status bar by calling the dialog box from a trusted application, such as Microsoft Visual Basic or an HTML Application (HTA), or from a trusted window, such as a trusted modal dialog box. These applications are considered to be trusted because they use Internet Explorer interfaces instead of the browser. Any dialog box generated from a trusted source has the status bar turned off by default. Resizing is turned off by default, but you can turn it on by specifying <code>resizable{{=}}yes</code> in the ''varOptions'' string of the '''showModalDialog''' method.
The default unit of measure for <code>dialogHeight</code> and <code>dialogWidth</code> in Internet Explorer 5 and later  is the pixel. The value can be an integer or floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For consistent results, specify the <code>dialogHeight</code> and <code>dialogWidth</code> in pixels when designing modal dialog boxes.
As of Microsoft Internet Explorer 4.0, you can eliminate scroll bars on dialog boxes. To turn off the scroll bar, set the [[html/attributes/scroll|'''SCROLL''']] attribute to <code>false</code> in the '''body''' element for the dialog window, or call the modal dialog box from a trusted application.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}