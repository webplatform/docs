{{Page_Title|Vibration API}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Provides access to the vibration mechanism of the hosting device. Vibration is a form of tactile feedback.}}
{{API_Listing}}
{{Concept_Listing
|Query=[[Category:Vibration]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=This API is specifically designed to address use cases that require simple tactile feedback only.

In the following example the device will vibrate for 1000 milliseconds (ms):

navigator.vibrate(1000); // or alternatively navigator.vibrate([1000]);

In the following example the pattern will cause the device to vibrate for 50 ms, be still for 100 ms, and then vibrate for 150 ms:

navigator.vibrate([50, 100, 150]);

The following example cancels any existing vibrations:

navigator.vibrate(0); // or alternatively navigator.vibrate([]);
}}
{{See_Also_Section
|Topic_clusters=Mobile
|External_links=* [http://www.w3.org/TR/vibration/ Vibration API]
* [http://www.w3.org/TR/2013/CR-vibration-20130723/ Vibration API - W3C Candidate Recommendation 23 July 2013]
* [http://www.w3.org/2009/dap/ Device APIs working group]
}}
{{Topics|API, Mobile, Vibration}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}