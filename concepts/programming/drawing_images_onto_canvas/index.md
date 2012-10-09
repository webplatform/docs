'''TODO:''' Add Descriptions and sample Code

* handle file select (e.target.files)
* window.URL.createObject(file) - plus polyfill
* create Image Element and load Object URL
* window.URL.removeObjectURL(img.src) - cleanup memory on-image-load
* draw scaled on Canvas (mention mobile Safari 2MB limit/issue - https://github.com/SunboX/ios-imagefile-megapixel)
* delete Image Element

'''"Retina" Canvas'''

* Explain "retina" Canvas drawing (http://html5-mobile.de/blog/retina-display-html-canvas-optimieren)

'''Alternatives'''

* FileReader.readAsDataURL(file) instead of window.URL.createObject(file) - pros/cons

'''Using WebGL for drawing?'''

* How does it work? (context 3d, shader)
* pros/cons (contra: no way to easy modify image pixels)
* Link to WebGL Convolution Matrix, Extented Color Transform Matrix "best practises"

'''Browser Compatibility'''

'''Links to used Object, Function Docs'''