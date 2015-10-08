# Digestable WebGL - Chapter 0.2: Checking for WebGL Support

## Checking for WebGL Support
Getting access to the API is a case of using JavaScript to get the *WebGL Context* which is called on a HTML canvas element. Browsers currently have two types of WebGL contexts:

```javascript
canvas.getContext('webgl'); // OR
canvas.getContext('experimental-webgl');
```

Different browsers use different arguments, but you can do away with this by testing for both as per [Modernizr](https://github.com/Modernizr/Modernizr/blob/master/feature-detects/webgl/extensions.js). The example (MIT License) is explained as such:

```javascript
try {
    var canvas = createElement('canvas'); // Get the canvas element
    var gl = canvas.getContext('webgl') || canvas.getContext('experimental-webgl');
    var exts = gl.getSupportedExtensions();
}
catch (e) {
    console.log("Failed to get WebGL context");
}
```

Alternatively you can use Modernizr itself to check for you (although that might be a bit overkill). The ctx.getSupportedExtensions function allows you to check for supported WebGL extentsions. We can ignore this for now, but if you require additional information check [here](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Using_Extensions)

## Creating A Blank WebGL Canvas

Let's dive straight in and create a blank canvas using WebGL. The sample cna be seen in the 'Code' folder of this repo, but here is the crux of the JavaScript:

```javascript
function startWebGL(){
    try {
        var canvas = document.getElementById("webgl-canvas");// Get the canvas element
        var gl = canvas.getContext('webgl') || canvas.getContext('experimental-webgl');
    }
    catch (e) {
        console.log("Failed to get WebGL context");
    }

    //Set the color to clear the canvas too : Red, Green, Blue, Alpha
    gl.clearColor(1.0, 0.0, 0.0, 1.0); // Red
    // gl.clearColor(0.0, 1.0, 0.0, 1.0); // Green
    //gl.clearColor(0.0, 0.0, 1.0, 0.3); // Transparent Blue
    // Clear the canvas
    gl.clear(gl.COLOR_BUFFER_BIT); //

}
startWebGL();
```
Here you can see all we do is get the WebGL context and clear its color to be Red (there are some other colours for you to play with too). We set the colour with gl.clearColor(1.0, 0.0, 0.0, 1.0) and we clear the screen to that colour with gl.clear(gl.COLOR_BUFFER_BIT). It is important to note because WebGL is based off OpenGL, colours are taken from 0 - 1 and not 0 - 255 as with CSS in web development. Once you've got that this sample should be simple enough!

## But What's a Buffer?
The easiest way to think of a buffer is an allocation in memory that stores some specific data that can be accessed by our WebGL program. In the case above we are storing our colors for clearing the canvas, but there are other built in buffers such as gl.DEPTH_BUFFER and gl.STENCIL_BUFFER but we'll come on those later.


## Credits and Sources

1. Mozilla Developer Network - [Using WebGL extensions]( https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Using_Extensions)
