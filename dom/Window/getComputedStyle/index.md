{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the final used values of all the CSS properties of an element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element that contains the desired style settings.
|Optional=No
}}{{Method Parameter
|Name=pseudoElementName
|Data type=String
|Description=The name of a CSS pseudo-element or a null value ("::before" or "::after"). Optional in WebKit based browsers.
|Optional=Yes
}}
|Method_applies_to=dom/window
|Example_object_name=window
|Return_value_name=declaration
|Javascript_data_type=CSSStyleDeclaration
|Return_value_description=A [[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']] object that contains the CSS settings applied to the desired object.

The settings in the returned object account for all applicable style rules and represent the final values for the various CSS properties applied to the specified object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var elem1 = document.getElementById("elemId");
var style = window.getComputedStyle(elem1, null);
 
// this is equivalent:
// var style = document.defaultView.getComputedStyle(elem1, null);
}}{{Single Example
|Language=HTML
|Code=&lt;style&gt;<br/> #elem-container{<br/>   position: absolute;<br/>   left:     100px;<br/>   top:      200px;<br/>   height:   100px;<br/> }<br/>&lt;/style&gt;<br/> <br/>&lt;div id=&quot;elem-container&quot;&gt;dummy&lt;/div&gt;<br/>&lt;div id=&quot;output&quot;&gt;&lt;/div&gt;  <br/> <br/>&lt;script&gt;<br/>  function getTheStyle(){<br/>    var elem = document.getElementById(&quot;elem-container&quot;);<br/>    var theCSSprop = window.getComputedStyle(elem,null).getPropertyValue(&quot;height&quot;);<br/>    document.getElementById(&quot;output&quot;).innerHTML = theCSSprop;<br/>   }<br/>  getTheStyle();<br/>&lt;/script&gt;
}}{{Single Example
|Language=HTML
|Description=getComputedStyle can pull style info off of pseudo-elements (for example, ::after, ::before, ::marker, ::line-marker).
|Code=<style>
 h3:after {
   content: ' rocks!';
 }
</style>
 
<h3>generated content</h3> 
 
<script>
  var h3       = document.querySelector('h3'), 
      result   = getComputedStyle(h3, ':after').content;
 
  console.log('the generated content is: ', result); // returns ' rocks!'
</script>
}}
}}
{{Notes_Section
|Notes=When the ''pseudoElementName'' is set to a value other than null, the value is interpreted as a CSS pseudo-element with respect to the object specified in the ''element'' parameter.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html
|Status=Recommendation
|Relevant_changes=Section 2.2.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/window.getComputedStyle
|HTML5Rocks_link=
}}