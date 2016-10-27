#Website Performance Optimization portfolio project

This project belongs to Udacity FEND in which students should optimize a specific site to make it run with a consistent frame-rate at 60fps and achieving also a PageSpeed score of at least 90 for Mobile and Desktop

###To run the Application

Site is hosted on GitHubPages [here](https://balusus.github.io/Website-Optimization/)

###Part 1: Optimize PageSpeed Insights score for index.html

The main changes to achieve the PageSpeed requested are the following ones:
    
   * Loading Google Fonts Asynchronously with Web Font Loader Script
   
   * Optimizing CSS Delivery inlining it in the HTML document as it's a small CSS file
   
   * Reducing all images sizes
 
   * Using Asynchronous Scripts so site is rendered and scripts are downloaded in the background
   
    
###Part 2: Optimize Frames per Second in pizza.html

The main changes to achieve a noteworthy FPS in pizza.html are the following ones:

 * Creating pizzas dinamically depending on the screen height instead of creating a huge fixed number of pizzas 
   when only a bunch of them are going to show.
   
 * Optimizing updatePositions function: Whenever a user scrolls, updatePosition is called, inside it there is 
   a for loop that is constantly changing pizzas position and recalculating scroll position so, in order not to make all          this calculations continuously, I took out that variable and put it outside the loop.
   
 * Changing querySelector with getElementsByClassName as is a faster way to access the DOM.
 
 * Scrolling event listener is changed so that udpatePosition function is not fired unnecessarily with                            requestAnimationFrame
