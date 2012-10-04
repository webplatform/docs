{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to declare a namespace when one of the default behaviors in Internet Explorer, clientCaps, is used as a custom tag in an HTML document. Note that the declared namespace (in this case, MSIE) is a prefix to the name of the default behavior in the custom tag. This example also shows how the clientCaps behavior can be used to install the Internet Explorer Data Binding component, if the component does not already exist in the user's system.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/behaviors/clientcaps/addDataBinding.htm
|Code=
&lt;HTML XMLNS:MSIE&gt;
&lt;HEAD&gt;
&lt;STYLE&gt;
@media all {
   MSIE\:clientCaps {behavior:url(#default#clientcaps);}
}
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
function window.onload()
{
   var bDataBindingAvailable  {{=}} false;
   var sDataBindingVersion {{=}} '';
   var sDataBindingID {{=}} 
       "{333C7BC4-460F-11D0-BC04-0080C7055A83}"; 
   bDataBindingAvailable {{=}} 
       oClientCaps.isComponentInstalled(sDataBindingID,"clsid");
   // if data binding is unavailable, install it
   if (!bDataBindingAvailable)
   {
      oClientCaps.addComponentRequest (sDataBindingID, 
          "componentid");
      bDataBindingAvailable {{=}} oClientCaps.doComponentRequest();
   }
   :
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY BGCOLOR{{=}}"#FFFFFF"&gt;
   :
   &lt;MSIE:CLIENTCAPS ID{{=}}"oClientCaps" /&gt;
   :
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can declare multiple namespaces on the '''html''' tag, as shown in the following syntax.
 <code>&lt;HTML XMLNS:Prefix1 XMLNS:Prefix2{{=}}"www.microsoft.com"&gt;</code>
The syntax for '''XMLNS''' is based on the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203781 W3C XML Namespace Spec]. Although the World Wide Web Consortium (W3C) document allows you to declare namespaces on all tags, Microsoft Internet Explorer 5 supports namespace declaration only on the '''html''' tag.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Requirements===
{| class="wikitable"
|-
!Minimum supported client
|Windows XP
|-
!Minimum supported server
|Windows Server 2003
|}

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>html</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}