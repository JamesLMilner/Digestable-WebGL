# Digestable WebGL - Chapter 0.1: Introducing WebGL

## Introduction
The purpose of this repo is to provide those without a background in graphics programming to understand WebGL by way of a series of step by step articles. I personally struggled to find relevant articles and content on WebGL so I'm putting these chapters together to share what I have leared with others. I more than encourage contributions or corrections. I try to cite sources where possible!

## What is WebGL?
Put plain and simply, WebGL 1.0 is a piece of technology you can utilize in the browser to build up a scene of 2D or 3D graphics.
It is based on OpenGL ES 2.0 which is a graphics API traditionally for embedded systems (phones, consoles and so forth). It provides a JavaScript API,
that can be leveraged, alongside the [HTML5 canvas element](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) to place graphics direclty onto a web page.

WebGL 1.0 was first incepted in 2006 at Mozilla, after which it was picked up by the Khronos Group (who maintain the specification). The WebGL specification was
released in 2011. WebGL 2.0 is currently in the works but don't worry about that too much for now!

Alongside a JavaScript API, WebGL also leverages something called 'shaders'. Shaders are essentially programs that tell the computer to draw a given set of geometries to the canvas in
a certain way. Shaders leverage the GPU (Graphical Process Unit) on the machine to render frames quickly ("GPUs are optimized for taking huge batches of data and performing the same operation
over and over very quickly" - NVIDIA, 2009). How GPUs work is a little outside the scope of these pages, but check out [this How Stuff Works article](http://computer.howstuffworks.com/graphics-card.htm) for more info.

We'll come on to shaders in more detail later on, so don't worry about
them too much at the moment. Just know they are vital to working with WebGL and help us draw things to our screen.

Shaders differ from another way of process graphics called 'Fixed Functions'. Fixed functions provide a well defined API for processing graphics through there various stages of the processing pipeline.

All you need to know is that Shaders are a more flexible and in some ways more powerful way of rendering than fixed functions, hence their deprecation in OpenGL 3.0 and WebGL 1.0.

## Why WebGL?
The main necessity for WebGL is the desire to provide 2D and 3D graphics natively within the browser (i.e. without plugins such as Flash). Many browser vendors are now looking to drop plugin support; Edge no longer supports ActiveX, Silverlight or Browser Helper Objects, Chrome no longer supports the Netscape Plugin API (NPAPI) which is responsible for Java, Silverlight and Unity Web Play among others.

Flash has been dying for a long time now along with Stage3D, with it's removal from Apple products leading the way on that. In order to graphics in the browser there was a necessity for something else,
especially in the case of 3D.  Whilst HTML5 brought the canvas API which provides a nice native API for 2D rendering, WebGL is also capable of immersive 3D scenes directly in the browser.

## Can I Use WebGL In This Browser?
All modern [evergreen](https://www.techopedia.com/definition/31094/evergreen-browser) browsers (IE 11+) have some level of WebgGL support. Check [caniuse.com/webgl](http://www.caniuse.com/webgl) or alternatively go to this site: [get.webgl.org](http://get.webgl.org).

## Should I Be Using WebGL?
There are many times when using WebGL might not be the best option. For example, if you are building a 2D simple game, and are not using any of the abstraction libraries for WebGL, the learning curve may be unnecessarily complex for such a use case. In this scenario [HTML canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) may be a better option. If you are wanting to build simple 2D games, check Microsoft's great [documentation on choosing the right API](https://msdn.microsoft.com/en-us/library/dn265058(v=vs.85)). If you want to build performant 2D or 3D experiences with lots of geometries and effects than WebGL is most likely the right choice for you.

## Is WebGL Hard?
This question very much depends on your development background. If you have a history in graphics programming, such as OpenGL or DirectX the learning curve may be a relatively smooth transition. If you are a web developer with limited experience in such technologies, the transition may be a little tougher. For a detailed explanation on why WebGL see [this explanation](http://learningwebgl.com/cookbook/index.php/WebGL:_Frequently_Asked_Questions#Why_is_coding_WebGL_so_hard.3F).



## Credits and Sources

1. Nvidia - [What’s the Difference Between a CPU and a GPU?]( http://blogs.nvidia.com/blog/2009/12/16/whats-the-difference-between-a-cpu-and-a-gpu/)
2. How Stuff Works - [How Graphics Cards Work](http://computer.howstuffworks.com/graphics-card.htm)
3. Microsoft - [WebGL, Canvas, or SVG? Choose the right API](https://goo.gl/jIOfji)
3. Learning WebGL - [Why is coding WebGL so hard?](http://learningwebgl.com/cookbook/index.php/WebGL:_Frequently_Asked_Questions#Why_is_coding_WebGL_so_hard.3F)
