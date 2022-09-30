---
layout: post
title:  "post-humanism"
date:   2022-09-10 14:12:29 +1000
categories: jekyll update
---

<!-- One of the artists that was mentioned in the assignment 2 brief included Qianqian Ye, their work includes heavy experimentation with p5, three.js, a lot of 3D and AR stuff which is super inspiring, through some thorough investigation (reading the About Me section) I had learnt that they hold a bachelors, and masters in Landscape Architecture. With an extremely strong background in the field, their work expands into 3D art and creative coding. Ye challenges social issues such as gender, immigrant, power and technology through her art.  -->

I wanted to express my appreciation towards my time in Digital Media and to celebrate why this course is so great and worthwhile, firstly, there has never been a time when I felt like my work had to be fixed or invalidated. What most of the lecturers do well in this course is to identify students' most important concerns, what drives their ambition. 

<!-- What Digital Media allows, is to gain all these different types of skills to be able to express our concerns and experiences, this is what creating is all about right? 

What the hell is this even all about anyway? this whole creating thing, being "creative" is just a way to extract what we deem inspiring in our minds, what we find cool from our past, our experiences, our traumas and projecting that into reality. Sometimes I forget why I create things, 

When we create or design, or ideate, what is it that we are projecting? Sometimes I might not even know it but, when you aren't limited to how you create, obviously the more expressive you become -->
Understanding Post-Humanism
the tldr version in my understanding - The social issues we face today stem from a, more or less, lack of humility in people caused by one's desire to selfishly achieve one's own benefit





"When you put energy into a website, in turn the website helps form your own identity" - Laurel Schwults

Thinking about websites as a form of world building.

- How can a website complement what you already do rather than competing or repeating?

In a world where everything feels so temporary, when life's moments, thoughts, feelings are always fleeting, maybe our desire for something more permanent becomes stronger.

- Cultivating your own garden. The metaphor is that you get to choose what you grow within that garden. 

Digital garden

<script type=module>

    // getting and formatting the canvas element
    const cnv = document.getElementById (`onclick_example`)
    cnv.width = cnv.parentNode.scrollWidth
    cnv.height = cnv.width * 9 / 16

    // this array will store the coordinates
    // of the click events
    const coordinates = []

    // this function will take the
    // pointerEvent as an argument
    // and assign it to parameter 'e'
    function add_coordinate (e) {

        // adding to the coordinates array 
        // an object with x & y properties
        // storing the values associated 
        // with the .offsetX and .offsetY
        // properties of the pointerEvent
        // object assigned to parameter 'e' 
        coordinates.push ({
            x : e.offsetX,
            y : e.offsetY
        })
    }

    // adding the function to the 
    // .onclick property of the canvas
    // add_coordinate
    cnv.onclick = add_coordinate

    // getting a 2d context
    const ctx = cnv.getContext ('2d')    

    // function to draw animation frames
    function draw_frame () {

        // turquoise background
        ctx.fillStyle = `turquoise`
        ctx.fillRect (0, 0, cnv.width, cnv.height)

        // hotpink squares
        ctx.fillStyle = `hotpink`

        // go through the coordinates array
        coordinates.forEach (p => {

            // use the values on the x & y properties
            // of each object to draw a square
            ctx.fillRect (p.x - 10, p.y - 10, 20, 20)
        })

        // call itself recursively
        requestAnimationFrame (draw_frame)
    }

    // call the first frame
    requestAnimationFrame (draw_frame)
</script>