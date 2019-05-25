### 1 slide
 > I am going to tell you about a canvas, mainly about the spheres where we can use it. First, I'll give you a piece of theory, tell you how to apply canvas in your project. Then in the main part I'll tell you about different ways to use canvas. In conclusion we'll compare canvas with other means of creating animation.

### 2 slide
> Nowadays canvas is a part of html5 specification. On the slide you can see official description of canvas. In simplier words, canvas is a HTML tag that defines a custom rectanglar drawing area within your web content.

> After being introduced by Apple in their OS X Dashboard canvas was adopted by almost all browsers.

> As it shown in the table, the most popular, major desktop and mobile browsers support canvas. For additional information you can see caniuse.com.

### 3 slide
> It is quite easy to start using canvas in a project. First of all you should add tag canvas in your html file. You can put some text between opening and closing tags if you want it to be shown in a case if a browser doesn't support canvas. After that it's required to define your drawing area in js by getting element by id. Each canvas object on a web page is intricately linked to a special JavaScript object called a 2D context object. So, after getting your canvas it is needed to get its context. After that you can start drawing. 

As soon as some objects has been created they get some state. The state includes the current transform, the fill and stroke colors, the current font, and a few other variables. You can save this state by pushing it onto a stack using the save() function. After you save the state you can make modifications, then restore to the previous state with the restore() function.
>
Learn more about canvas methods you can using this cheatsheet.
 
> Another thing which is essential to know about is canvas grid or coordinate space. Normally one unit in the grid corresponds to one pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin.

### 4 slide
> Here you see several ways for using canvas. I can't but mention that it is non-exhaustive list. Besides drawing, unusual typographic effects, creating animations and games, canvas is widely used to manipulate images, create graphs, charts and also for adding some effects to video and audio, for instance, chroma-key to video or visualisation to music. 
It's time to move on to examples. In most cases I'll show you a simple and complicated implementations.

### 5 slide
> It's important to understand that Canvas is for drawing pixels. It doesn't have shapes or vectors. There are no objects to attach event handlers to. 

> In this example you can see how it is easy to draw a rectangle. It's enough to set the current color and a fill an area with a needed shape. 
Canvas only directly supports the rectangle shape.

> To draw any other shape you must draw it yourself using a path. Paths are shapes created by a bunch of straight or curved line segments. In Canvas you must first define a path with beginPath(), then you can fill it, stroke it, or use it as a clip. You define each line segment with functions like moveTo(), lineTo(), and bezierCurveTo().
This example draws a shape with a move to, followed by a bezier curve segment, then some lines. After creating the path it fills and strokes it.

> The basic steps in building a path are as follows:

+ Start building the path by opening a new path with beginPath.
+ Define the starting point of the new subpath using the moveTo method.
+ Add one or more segments to the subpath using such methods as lineTo and quadraticCurveTo.
+ Repeat steps 2 and/or 3 until the path is defined.
+ Optionally, call closePath to connect the path’s start and end points with a straight line.

> As an example of complicated implementation is an online copy of Paint in canvas with all familiar functionality.

### 6 slide

> Text-effects with canvas is not the thing to speak frequently as it seems to be easier to manipulate text with help of css. However canvas gives an opportunity to create unusual effects with gradients, shadows, transformations.

> Here is an examle of ordinary text. You need to choose font and color and call needed method.

> And here is a small part of opportunies with which canvas provides us.

### 7 slide

> Canvas gives us an opportunity to manipulate sprites, make moving background.

> The steps to create canvas animation are following:

+ Clear the canvas contents (e.g. with fillRect() or clearRect()).
+ Save state (if necessary) using save()
+ Draw the graphics you are animating.
+ Restore the settings you saved in step 2, using restore()
+ Call requestAnimationFrame() to schedule drawing of the next frame of the animation.
 
The requestAnimationFrame method provides a smoother and more efficient way for animating by calling the animation frame when the system is ready to paint the frame. The number of callbacks is usually 60 times per second and may be reduced to a lower rate when running in background tabs.

> Here I'll show you a couple of experiments with canvas:
> matrix and
> attemption to repeat movements of cloth.

### 8 slide
> Canvas is frequently used to create games as it has all necessary tools.
> Many of games are rather simple. Their sense is to earn points for some acrions. Usually these games serve to kill time.

### 9 slide
> There are four ways to draw things on the web: Canvas, SVG, CSS, and direct DOM animation. Canvas differ from the other three:

SVG: SVG is a vector API that draws shapes. Each shape has an object that you can attach event handlers to. If you zoom in the shape stays smooth, whereas Canvas would become pixelated.

CSS: CSS is really about styling DOM elements. Since there are no DOM objects for things you draw in Canvas you can't use CSS to style it. CSS will only affect the rectanglar area of the Canvas itself, so you can set a border and background color, but that's it.

DOM animation: The DOM, or Document Object Model, defines an object for everything on the screen. DOM animation, either by using CSS or JavaScript to move objects around, can be smoother in some cases than doing it with Canvas, but it depends on your browser implementation.

Canvas is lower level than those others so you can have more control over the drawing and use less memory, but at the cost of having to write more code.

> Use SVG when you have existing shapes that you want to render to the screen.

Use CSS or DOM animation when you have large static areas that you wish to animate, or if you want to use 3D transforms.

For charts, graphs, dynamic diagrams, and of course video games, Canvas is a great choice.

### 10 slide
> Summarizing, canvas is a powerful tool which serves different purposes. Canvas can be used to manipulate pixels in images, to create animations, typographic effects, to add some unusual background in videos or to visualize music. It is reasonable to apply canvas when you want to make some charts, graphs, diagrams, video games.
That's it. Thank you for your attention!