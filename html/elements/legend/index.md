{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Compatibility.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''legend''' element represents a title or explanatory caption for the contents of its parent '''fieldset''' element.}}
{{Markup_Element
|DOM_interface=dom/HTMLLegendElement
|Content=The '''legend''' element represents a caption for the the contents of the legend element's parent fieldset element, if any.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Simple form with fieldset, legend, and label elements.
|Code=<form action="" method="post">
  <fieldset>
    <legend>User credentials</legend>
    <label for="username">Username</label>
    <input type="text" name="username" id="username">
    <label for="password">Password</label>
    <input type="password" name="password" id="password"> 
  </fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/8e4305d9f7fb613410a5
}}
}}
{{Notes_Section
|Usage=Generally, the '''legend''' element can be used in combination with a '''fieldset''' element when a group of form elements needs a caption. Pretty similar to a headline element but the '''legend''' element is the most semantic element in that case.
|Notes=The first '''legend''' element in a '''fieldset''' is used as the caption of the '''fieldset'''. Additional '''legend''' elements are ignored.
|Import_Notes=The '''legend''' element will be placed within the border of the '''fieldset''' element if you are using a fieldset and leaving the default browser styles untouched. The position will change as soon as you set <code>border: none;</code> to your fieldset.

The »problem« with the '''fieldset''' and '''legend''' elements is that they don’t behave like normal block/inline elements. A general workaround with any styling and position issues (especially in old IEs) is to wrap your legends content with another element. 

<syntaxhighlight>
<fieldset>
  <legend><span>Legend link</span></legend>
</fieldset>
</syntaxhighlight>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#the-legend-element
|Status=Candidate Recommendation
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
|Topic_clusters=HTML
|Manual_links=* [[html/elements/form|'''form''']] element
* [[html/elements/fieldset|'''fieldset''']] element
|External_links=* http://www.w3.org/TR/html-markup/legend.html#legend
* http://www.w3.org/TR/html5/forms.html#the-legend-element
* http://morten.dk/blog/fieldset-legend-behave
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}