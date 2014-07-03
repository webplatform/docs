{{Page_Title|Vibration API}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The Vibration API provides access to the vibration mechanism of the hosting device. Vibration is a form of tactile feedback, often used by mobile phones.}}
{{API_Listing}}
{{Concept_Listing
|Query=[[Category:Vibration]][[Category:API_Objects]]
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=This API is specifically designed to address use cases that require simple tactile feedback only. This API is not meant to be used as a generic notification mechanism. Such use cases may be handled using the Web Notifications specification.

In the following example the device will vibrate for 1000 milliseconds (ms):

<syntaxhighlight lang="javascript">
navigator.vibrate(1000);
// or alternatively
navigator.vibrate([1000]);
</syntaxhighlight>

In the following example the pattern will cause the device to vibrate for 50 ms, be still for 100 ms, and then vibrate for 150 ms:

<syntaxhighlight lang="javascript">
navigator.vibrate([50, 100, 150]);
</syntaxhighlight>

The following example cancels any existing vibrations:

<syntaxhighlight lang="javascript">
navigator.vibrate(0);
// or alternatively
navigator.vibrate([]);
</syntaxhighlight>
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