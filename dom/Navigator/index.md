{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=New listing page with proper object capitalization; replaces '''navigator'''.
|Checked_Out=Yes
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|The navigator object contains state and identity information about the browser/user agent.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=[object Navigator] example enumerates the window.navigator object and displays the results in the web page.
|Code=   var output = document.getElementById('divOutput');
   var html='<h2>[object Navigator]<\/h2>';
   for(p in window.navigator){
   
			html+='<label style=\"color:navy\">navigator.'+p+':<br/><input style=\"width:100%\" type=\"text\" value=\"'+eval('window.navigator.'+p)+'\"/><\/label><br/>';
   }
   output.innerHTML=html;

|LiveURL=http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788
}}
}}
{{Notes_Section
|Usage=Commonly used for feature detection of a web browser capabilities. java RTE and cookie support.
Avoid UserAgent sniffing of the navigator.userAgent property as this is not a reliable indicator of the userAgent's actual version number.
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Navigator Navigator Object]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms535867(v=vs.85).aspx Navigator Object]
|HTML5Rocks_link=
}}
{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}