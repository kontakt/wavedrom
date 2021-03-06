## WaveDrom Skin

WaveDrom rendering engine uses SVG template (skin) to create output diagram.
Effectively the skin contains building blocks (bricks) of different parts of waveform graphics.
Each brick is an SVG group with unique id. WaveDrom engine will include template into
every diagram picture and build picture referencing to elements with specific ids.

[default.svg](https://github.com/drom/wavedrom/blob/master/unpacked/skins/default.svg)

### Drawing the skin

Users can define their own skin in order to change the visual properties of the resulting timing diagram.
The [Inkscape](http://inkscape.org/) editor can be used to draw the skin.

See 
[default.svg](https://github.com/drom/wavedrom/blob/master/unpacked/skins/default.svg) and
[narrow.svg](https://github.com/drom/wavedrom/blob/master/unpacked/skins/narrow.svg)
sources for example.

### Packing the skin

The source skin SVG needs to be converted by
[bin/svg2js.js](https://github.com/drom/wavedrom/blob/master/bin/svg2js.js)
script in order to be used by WaveDrom.

The resulted JSON file is much smaller in size and has meta-information needed for WaveDrom to work.

See the example of packed skin:
[default.js](https://github.com/drom/wavedrom/blob/master/skins/default.js)
[narrow.js](https://github.com/drom/wavedrom/blob/master/skins/narrow.js)
