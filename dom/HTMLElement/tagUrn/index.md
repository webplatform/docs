{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the values returned by the '''scopeName''' and '''tagUrn''' properties to create a simple HelloWorld custom tag.

The browser's status bar displays the property values.

'''Note'''  For IE8Standards mode to render correctly, make sure there is no spaces in your call to the HTC file.
|Code=&lt;HTML XMLNS:InetSDK{{=}}'http://msdn.microsoft.com/workshop'&gt;

&lt;STYLE&gt;
@media all {
   InetSDK\:HelloWorld { behavior:url(simple.htc) }
}
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
   function window.onload()
   {
      window.status {{=}} 'scopeName {{=}} ' + hello.scopeName +
                      '; tagUrn {{=}} '  + hello.tagUrn;
   }
&lt;/SCRIPT&gt;
&lt;BODY&gt;
   &lt;InetSDK:HelloWorld ID{{=}}'hello'&gt;&lt;/InetSDK:HelloWorld&gt;
   
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tagUrn.htm
}}{{Single Example
|Description=An alternative call to the HTC can also be made as an attribute, as shown in the following code example.
|Code=&lt;HTML XMLNS:InetSDK{{=}}'http://msdn.microsoft.com/workshop'&gt;

&lt;SCRIPT&gt;
   function window.onload()
   {
      window.status {{=}} 'scopeName {{=}} ' + hello.scopeName +
                      '; tagUrn {{=}} '  + hello.tagUrn;
   }
&lt;/SCRIPT&gt;
&lt;BODY&gt;
   &lt;InetSDK:HelloWorld ID{{=}}'hello' style{{=}}"behavior:url(simple.htc)"&gt;&lt;/InetSDK:HelloWorld&gt;
   
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL='''Note'''  Make sure there are no spaces in your style's declaration.
}}
}}
{{Notes_Section
|Notes====Remarks===
To declare the namespace in the document, use the [[apis/xhr/properties/XMLNS attribute|'''XMLNS''']] attribute of the '''html''' element.
Download the HTC for the sample below: [http://go.microsoft.com/fwlink/p/?linkid{{=}}203827 simple.htc]
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