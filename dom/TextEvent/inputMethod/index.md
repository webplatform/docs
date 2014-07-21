{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Gets a value that describes how text is entered.}}
{{API_Object_Property
|Property_applies_to=dom/TextEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=inputMethod
|Javascript_data_type=Number
|Return_value_description=The input method used to generate the event.
One of the following values -
*TextEvent.DOM_INPUT_METHOD_UNKNOWN       = 0
*TextEvent.DOM_INPUT_METHOD_KEYBOARD      = 1
*TextEvent.DOM_INPUT_METHOD_PASTE         = 2
*TextEvent.DOM_INPUT_METHOD_DROP          = 3
*TextEvent.DOM_INPUT_METHOD_IME           = 4
*TextEvent.DOM_INPUT_METHOD_OPTION        = 5
*TextEvent.DOM_INPUT_METHOD_HANDWRITING   = 6
*TextEvent.DOM_INPUT_METHOD_VOICE         = 7
*TextEvent.DOM_INPUT_METHOD_MULTIMODAL    = 8
*TextEvent.DOM_INPUT_METHOD_SCRIPT        = 9
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Display a user friendly value of the inputMethod property of an event.
|Code=var description=(event.inputMethod)?getDOMInputMethod(event.inputMethod):'not supported';

    function getDOMInputMethod(iInputMethod){
    	switch (iInputMethod){
    		case TextEvent.DOM_INPUT_METHOD_UNKNOWN:// 0
    			return 'Unknown';
    		case TextEvent.DOM_INPUT_METHOD_KEYBOARD:// 1
    			return 'Keyboard';
    		case TextEvent.DOM_INPUT_METHOD_PASTE:// 2
    			return 'Paste';
    		case TextEvent.DOM_INPUT_METHOD_DROP:// 3
    			return 'Drop';
    		case TextEvent.DOM_INPUT_METHOD_IME:// 4
    			return 'IME';
    		case TextEvent.DOM_INPUT_METHOD_OPTION:// 5
    			return 'Option';
    		case TextEvent.DOM_INPUT_METHOD_HANDWRITING:// 6
    			return 'Handwriting';
    		case TextEvent.DOM_INPUT_METHOD_VOICE://7
    			return 'Voice';
    		case TextEvent.DOM_INPUT_METHOD_MULTIMODAL: // 8
    			return 'MultiModal';
    		case TextEvent.DOM_INPUT_METHOD_SCRIPT://9
    			return 'Script';
    		default:
    			return 'Unknown';
    	}
    }

}}
}}
{{Notes_Section
|Usage=Use to determine if the device that initiated the textinput event is to be 'trusted'.

|Notes=Not implemented in Safari or Chromium.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events (20110531)
|URL=http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531
|Status=Outdated Working Draft
|Relevant_changes=Section 5.2.5
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974806(v=vs.85).aspx inputMethod Property]
|HTML5Rocks_link=
}}