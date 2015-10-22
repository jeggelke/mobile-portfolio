## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

#####Changes I made

* Resized ```pizzeria.jpg``` image
* Added async to Google Analytics Script
* Added media attribute to Print stylesheet
* Replaced ```style.css``` with inline styles
* Replaced Google Font stylesheet with ```webfont.js```
* Compressed ```profilepic.jpg```

####Part 2: Optimize Frames per Second in pizza.html

#####Changes I made

* Used optimization from [quiz](https://www.udacity.com/course/viewer#!/c-ud860-nd/l-4147498575/e-4154208580/m-4240308553) to fix pizza resizing
* Replaced ```querySelectorAll``` with ```getElementsByClassName``` and ```getElementById```
* Created ```animationReadyCheck()``` to handle ```requestAnimationFrame```, which runs ```updatePositions()```
* Moved ```document.body.scrollTop / 1250``` out of for loop as it does not need to be declared several times
* Changed ```items[i].style.left = items[i].basicLeft + 100 * phase + 'px'``` to use a transform method to prevent layout thrashing
* Removed height/width during each ```movingPizzas``` iteration. Handling this with css instead
* Moved ```window.items = document.getElementsByClassName('mover')``` from being called on each scroll
