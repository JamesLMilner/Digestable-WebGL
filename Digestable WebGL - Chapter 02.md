# Digestable WebGL - Chapter 0.2: The WebGL API

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
    var ctx = canvas.getContext('webgl') || canvas.getContext('experimental-webgl');
    var exts = ctx.getSupportedExtensions();
}
catch (e) {
    return;
}
```

Alternatively you can use Modernizr itself to check for you (although that might be a bit overkill).

## Creating A Blank WebGL Canvas





## Credits and Sources

1. Nvidia - [What’s the Difference Between a CPU and a GPU?]( http://blogs.nvidia.com/blog/2009/12/16/whats-the-difference-between-a-cpu-and-a-gpu/)
2. How Stuff Works - [How Graphics Cards Work](http://computer.howstuffworks.com/graphics-card.htm)
3. Microsoft - [WebGL, Canvas, or SVG? Choose the right API](https://goo.gl/jIOfji)
3. Learning WebGL - [Why is coding WebGL so hard?](http://learningwebgl.com/cookbook/index.php/WebGL:_Frequently_Asked_Questions#Why_is_coding_WebGL_so_hard.3F)
