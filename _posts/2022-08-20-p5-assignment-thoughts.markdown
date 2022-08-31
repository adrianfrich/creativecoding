---
layout: post
title:  "p5 assignment thoughts"
date:   2022-08-20 14:12:29 +1000
categories: jekyll update
---

Here is an early progress p5 sketch of the assignment
<iframe src="https://editor.p5js.org/adrianfrich/full/ln7OC2rex" width="576" height="324"></iframe>

By utilising a lot of WEBGL elements into the p5 sketch, I was able to use various 3D shapes to form a planet-like animated graphic - which I'm all over for, I'd love to have something showcased like this on my personal folio. I combined a rotating rotating torus with a rotating cube spinning in the opposite direction so it looked a little bit more chaotic. 

{% highlight ruby %}
    function draw () {
    background(175);
    rotateX(angle);
    rotateY(angle * 0.3);
    rotateZ(angle * 1.2);

    normalMaterial();
    noStroke();
    torus(100,10);
{% endhighlight %}




Here is the finished product of the assignment. Overall I found the experience quite challenging at first, I had to revisit a lot of tutorials, a lot of experimenting with lighting, using the ambientLight function to play around with different light sources which I had ended up scrapping. I think this is something I would play around with in the future as well. A lot of elements in this assignment came about by accident naturally, but in the end I made sure to understand how those elements came to be. For example the trail effect happens because javascript is constantly refreshing the function draw, so when you tell it to make a rotate shape appear in the frame while simultaneously having the ability to move the "camera" around using the perspective function, you are then able to have this cool painting effect with the desired rotating shapes.

<iframe src="https://editor.p5js.org/adrianfrich/full/BTtTPSQCL" width="576" height="324"></iframe>
<br>
<br>

Building on top of this, the assignment called for text elements and branding to be included, so at this stage I needed to figure out how to put text on the rotating cube - this proved to be the most difficult part of the sketch. Only because I haven't discovered the createGraphics function at this stage. But by using this function, you are able to call a texture function onto the cube itself and it will replace all faces of the cube with whatever you have in the setup.

{% highlight ruby %}
    text = createGraphics(300, 100);
    text.fill(230, 30, 42);
    text.textAlign(CENTER);
    text.textFont(museo);
    text.textSize(50);
    text.text("RMIT", 140, 50);
{% endhighlight %}

{% highlight ruby %}
    texture(text);
    box(90);
{% endhighlight %}

Ideas that I'd like to implement to future projects/learn how to do: 
- Sound elements with interactibility, playing around with looping and drum loops
- controllable game within website
- rotatable 3D models with scrollable gallery-like feature using the scroll mouse wheel. 

<iframe src="https://editor.p5js.org/adrianfrich/full/BTtTPSQCL" width="576" height="324"></iframe>