{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Exposes a high precision timestamp to developers so they can better measure the performance of their applications.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script shows how a developer can use the interfaces defined in this document to obtain timing data related to developer scripts.
|Code=function init() {
	performance.mark("startTask1");
	doTask1(); // Some developer code
	performance.mark("endTask1");
				
	performance.mark("startTask2");
	doTask2(); // Some developer code
	performance.mark("endTask2");

	measurePerf();
}

function measurePerf() 
{
	var perfEntries = performance.getEntriesByType("mark");
	
	for (var i = 0; i < perfEntries.length; i++)
   	{
		if (window.console) console.log("Name: " + perfEntries[i].name + 
						" Entry Type: " + perfEntries[i].entryType +
						" Start Time: " + perfEntries[i].startTime + 
						" Duration: "   + perfEntries[i].duration  + "\n");
   }
}

window.addEventListener('load', init, false);
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C User Timing Specification
|URL=http://www.w3.org/TR/user-timing/
|Status=W3C Candidate Recommendation
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
{{Topics|User Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}