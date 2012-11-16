{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Creates a WaveTable representing a waveform containing arbitrary harmonic content. The real and imag parameters must be of type Float32Array of equal lengths greater than zero and less than or equal to 4096 or an exception will be thrown. These parameters specify the Fourier coefficients of a Fourier series representing the partials of a periodic waveform. The created WaveTable will be used with an OscillatorNode and will represent a normalized time-domain waveform having maximum absolute peak value of 1. Another way of saying this is that the generated waveform of an OscillatorNode will have maximum peak value at 0dBFS. Conveniently, this corresponds to the full-range of the signal values used by the Web Audio API. Because the WaveTable will be normalized on creation, the real and imag parameters represent relative values.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=real
|Data type=String
|Description=Represents an array of cosine terms (traditionally the A terms). In audio terminology, the first element (index 0) is the DC-offset of the periodic waveform and is usually set to zero. The second element (index 1) represents the fundamental frequency. The third element represents the first overtone, and so on.
|Optional=No
}}{{Method Parameter
|Name=imag
|Data type=String
|Description=Represents an array of sine terms (traditionally the B terms). The first element (index 0) should be set to zero (and will be ignored) since this term does not exist in the Fourier series. The second element (index 1) represents the fundamental frequency. The third element represents the first overtone, and so on.
|Optional=No
}}
|Method_applies_to=apis/webaudio/AudioContext
|Example_object_name=AudioContext
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}