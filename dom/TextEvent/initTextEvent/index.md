{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Initializes a new text event that the createEvent method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|'''type''']] property.
This parameter is case sensitive! Sets the type property of the event object.

For IE9 or higher use 'textinput'
For Webkit use 'textInput'.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/Event/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/Event/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=view
|Data type=Object
|Description=The window on which this event is occurring. Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=data
|Data type=String
|Description=Character data. Sets the value for the [[dom/CompositionEvent/data|'''data''']]  property.
|Optional=No
}}{{Method Parameter
|Name=inputMethod
|Data type=Number
|Description=The input mode for the text. Sets the value for the [[dom/TextEvent/inputMethod|'''inputMethod''']] property.

Required in Internet Explorer, not supported and omitted in Safari and Google Chrome. Integer that specifies the input mode for the text.
|Optional=No
}}{{Method Parameter
|Name=locale
|Data type=String
|Description=The locale name. Sets the value for the [[dom/CompositionEvent/locale|'''locale''']] property.

Required in Internet Explorer, not supported and omitted in Safari and Google Chrome. String that specifies the locale name of the text.
|Optional=No
}}
|Method_applies_to=dom/TextEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The below sample shows a click event handler that creates and dispatches either a 'textinput' or 'textInput' event (depending on the selected options) to textarea element.
|Code=function InsertText () {
        try {
            var newtextEvent {{=}} document.createEvent('TextEvent');
            var textarea {{=}} document.getElementById ("textarea");
            var intputmethod{{=}}eval(document.getElementById('cboinputmethod').value);
			if(document.forms.frmTextEvent.chkontextinput.checked){
            //var retval = TextEvent.initTextEvent(eventType, canBubble, cancelable, viewArg, dataArg, inputMethod, locale); 
            	newtextEvent.initTextEvent ('textinput', true, true, null, "New text", intputmethod, "en-US");
            }
            else if(document.forms.frmTextEvent.chkontextInput.checked){
            	newtextEvent.initTextEvent ('textInput', true, true, null, "New text", intputmethod, "en-US");
            }else{
            	alert('First choose the textinput or textInput event handler.'); return;
            }
            //var selObj=window.getSelection();
            textarea.focus();
            textarea.selectionStart {{=}} 0;
            textarea.selectionEnd {{=}} 0;

            textarea.dispatchEvent(newtextEvent);
        }
        catch (e) {
            alert ('Your browser does not support this example!\nError :'+e);
        }
    }


// Outputs 'New text' at the beginning of the text area in Safari and Chromium
// Outputs nothing at the beginning of a the text area in MSIE browsers as DOM_INPUT_METHOD_SCRIPT is not a trusted (event.isTrusted) textinput input method.
}}{{Single Example
|Language=JavaScript
|Description=The DOMInputMetod is present in the MSIE 'textinput' event handler only.
|Code=function getDOMInputMethod(iInputMethod){
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
|Usage=Used to emulate keyboard events from other input devices like on screen keyboard clicks, voice input, handwriting, copy and paste operations and scripted input methods.
|Notes=The event type is case sensitive!

In Internet Explorer use 'textinput' for the eventType.

In Safari and Chromium use 'textInput' for the eventType parameter.

MSIE browsers further require that the event inputMethod isTrusted.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975268(v=vs.85).aspx initTextEvent Method]
|HTML5Rocks_link=
}}