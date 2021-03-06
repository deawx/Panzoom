# Panzoom
Panzoom is a lightweight native JavaScript library for panning and zooming elements using CSS3 Transformations. It's built to have a small footprint and be and simple to use.

## Installation

You can grab the latest version by linking to CDN:

    <script src="https://cdn.rawgit.com/SpencerWie/Panzoom/1cc9755f/dist/panzoom.min.js"></script>

Or clone this Repository and link to the code:

    <script src="path/to/repo/dist/panzoom.min.js"></script>

## How to use

Simply call the method `PanZoom` like so:

    PanZoom(selector, [settings]);
    
That's it! Now all your elements given by your selector will now have basic panning and zoomming functionality. For example, we could have the class `panzoom` which has many elements:

    <h1 class="panzoom">Hello World!</h1>
    <img class="panzoom" src=".." .. />
    <div class="panzoom" .. >Foo Bar</div>
    <canvas class="panzoom" ..></canvas>

Our JavaScript code for applying Panzoom on these elements would be:

    PanZoom(".panzoom");


## Settings

The second parameter takes an object which can be used to customize the settings of Panzoom, the following keys can be used:

* **minScale**&nbsp;&nbsp;&nbsp;[`Number | default = 0.1`]: The smallest value an image can be zoomed into.
* **maxScale**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[`Number | default = 5`]: The largest value an image can be zoomed into. 
* **increment**[`Number | default = 0.05`]: How much to zoom on an image on each zoom event. 
* **liner**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[`Boolean | default = false`]: Whether to zoom linearly or non-lineraly when using _increment_. Non-linery scales more the closer you are the the image and less when further away.

An example of using custom settings:

    PanZoom(".panzoom", {minScale: 0.2, maxScale: 3, increment: 0.1, liner: true});

## Demos

* [Demo using HTML 5 Canvas](https://cdn.rawgit.com/SpencerWie/Panzoom/b070fa28/demo/CanvasExample/index.html)
* [Demo using SVG Image](https://cdn.rawgit.com/SpencerWie/Panzoom/b070fa28/demo/SvgExample/index.html)
