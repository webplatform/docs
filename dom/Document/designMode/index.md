{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets or gets a value that indicates whether the document can be edited.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=designMode
|Javascript_data_type=String
|Return_value_description="on" if the the document is editable, or "off" if it is not. Default is "off".
|Example_value_name=newDesignMode
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example toggles the state of document.designMode when the window is double-clicked.
|Code=<!DOCTYPE HTML>
<html>
<head>
<script>
window.ondblclick = toggleDesignMode;

function toggleDesignMode() {
  alert(document.designMode);
  document.designMode = (document.designMode == "on") ? "off" : "on";
  alert(document.designMode);
}
</script>
</head>

<body>
<p>This is a paragraph, which may or may not be editable.</p>
</body>
</html>

}}
}}
{{Notes_Section
|Usage=Use the '''designMode''' property to let the user edit the current document.
While the browser is in design mode, objects enter a UI-activated state when the user presses <code>ENTER</code>, clicks an object that has focus, or double-clicks the object. Objects that are UI-activated have their own window in the document. You can modify the UI only when the object is in a UI-activated state.
|Notes=*You cannot execute script when the value of the '''designMode''' property is set to '''on'''.
*The default value is '''off'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 3.1.1
}}
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