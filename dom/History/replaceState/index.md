{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Overwrites the current history record with a new record.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=statedata
|Data type=DOM Node
|Description=The data to update.
|Optional=No
}}{{Method Parameter
|Name=title
|Data type=String
|Description=The data title to update.
|Optional=No
}}{{Method Parameter
|Name=url
|Data type=String
|Description=The data URL to update.
|Optional=Yes
}}
|Method_applies_to=dom/history
|Example_object_name=history
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, a user stored a preference where they want to go straight to the User Account page when they go to the homepage of the website. The code checks for such preference and replaces the URL shown by the browser accordingly and shows a User Account page (albeit minimal).
This way, there will be no history record for the original homepage of the website, only for the User Account page.
|Code=if (localStorage["first-page"] === "account") {
 window.history.replaceState({"page": "account", "User Account", "/account");
 document.body.innerHTML = "<h1>User Account</h1>";
}
}}
}}
{{Notes_Section}}
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