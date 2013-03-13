{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Replaces the current transformation matrix with the result of multiplying the current transformation matrix with the matrix described by:

<code>a c e<br/>
b d f<br/>
0 0 1</code>
}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=a
|Data type=any
|Description=The  m1,1  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=b
|Data type=any
|Description=The  m1,2 value  in the matrix.
|Optional=No
}}{{Method Parameter
|Name=c
|Data type=any
|Description=The  m2,1  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=d
|Data type=any
|Description=The  m2,2  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=e
|Data type=any
|Description=The delta x (dx)  value in the matrix.
|Optional=No
}}{{Method Parameter
|Name=f
|Data type=any
|Description=The  delta y (dy)  value in the matrix.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=working live example that shows visually how the transformation matrix works.
|LiveURL=http://www.audiocommander.de/dev/HTML5/transform.html
}}{{Single Example
|Language=HTML
|Description=This example shows visually how the transformation matrix works.
|Code=<html>
<head>
	<title>Transformation Matrix Demo</title>

<style>
#sliders {
	position: absolute;
	left: 0;
	top: 0;
}
#slA,#slB,#slC,#slD,#slE,#slF {
	display: block;
	position: relative;
	top: 1em;
	z-index: 100;
	margin-bottom: 2em;
}
</style>
</head>

<body>
<canvas id="canvas" width="800" height="600"></canvas>
<div id="sliders">
<div id="slA"><input type="range" id="sliderA" min="-100" max="100" value="100"></input>a:<span id="aValue">0</span></div>
<div id="slB"><input type="range" id="sliderB" min="-100" max="100" value="0">	</input>b:<span id="bValue">0</span></div>
<div id="slC"><input type="range" id="sliderC" min="-100" max="100" value="0">	</input>c:<span id="cValue">0</span></div>
<div id="slD"><input type="range" id="sliderD" min="-100" max="100" value="100"></input>d:<span id="dValue">0</span></div>
<div id="slE"><input type="range" id="sliderE" min="-100" max="100" value="0">	</input>e:<span id="eValue">0</span></div>
<div id="slF"><input type="range" id="sliderF" min="-100" max="100" value="0">	</input>f:<span id="fValue">0</span></div>
</div>

<script type="text/javascript">

var canvas = document.getElementById("canvas");
var ctx = canvas.getContext('2d');

// get the sliders
var sliderA = document.querySelector('#sliderA');
var sliderB = document.querySelector('#sliderB');
var sliderC = document.querySelector('#sliderC');
var sliderD = document.querySelector('#sliderD');
var sliderE = document.querySelector('#sliderE');
var sliderF = document.querySelector('#sliderF');

var a, b, c, d, e, f;

function mapSliderValue(v) {
	return v / 100;
}

function sliderDidChange() {
	// get values
	a = mapSliderValue(sliderA.value);
	b = mapSliderValue(sliderB.value);
	c = mapSliderValue(sliderC.value);
	d = mapSliderValue(sliderD.value);
	e = sliderE.value;
	f = sliderF.value;
	// show values
	document.querySelector('#aValue').innerText = a;
	document.querySelector('#bValue').innerText = b;
	document.querySelector('#cValue').innerText = c;
	document.querySelector('#dValue').innerText = d;
	document.querySelector('#eValue').innerText = e;
	document.querySelector('#fValue').innerText = f;
	// redraw
	draw();
}

function draw() {
	// save the current context
	ctx.save();
	// clear background
	ctx.fillStyle = "lightsteelblue";
	ctx.fillRect(0,0,canvas.width,canvas.height);
	// apply transform matrix
	ctx.setTransform(a, b, c, d, e, f);
	// draw transformed text
	ctx.fillStyle = "navy";
	ctx.fillText("Hello World!", 0, 0);
	// restore the context
	ctx.restore();
}

function setup() {
	ctx.font = "5em Arial";
	// set default values for tx & ty
	sliderE.min = 0;
	sliderE.max = canvas.width;
	sliderE.value = (canvas.width / 2) - (ctx.measureText("Hello World!").width / 2);
	sliderF.min = 0;
	sliderF.max = canvas.width;
	sliderF.value = canvas.height / 2;
	// add Event listeners
	sliderA.addEventListener("change",sliderDidChange,false);
	sliderB.addEventListener("change",sliderDidChange,false);
	sliderC.addEventListener("change",sliderDidChange,false);
	sliderD.addEventListener("change",sliderDidChange,false);
	sliderE.addEventListener("change",sliderDidChange,false);
	sliderF.addEventListener("change",sliderDidChange,false);
	sliderDidChange();
}

setup();

</script>

</body>
</html>
|LiveURL=http://audiocommander.github.com/transformMatrixDemo
}}
}}
{{Notes_Section
|Notes=The parameters of ''transform'' represent a matrix. This matrix is multiplied with the transformation matrix of the current context.

The arguments ''a, b, c, d, e, f'' are sometimes called ''m11, m12, m21, m22, dx, dy'' or ''m11, m21, m12, m22, dx, dy''. Care should be taken in particular with the order of the second and third arguments (''b'' and ''c'') as their order varies from API to API; APIs sometimes use the notation ''m12/m21'' and sometimes ''m21/m12'' for those positions.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0-7.0 (partial)
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}