## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To inspect the site run the index.html.  Or if want to experience the web option follow the above steps in order to run as a local server:

	** open one terminal window 
	** cd /path/to/your-project-folder
	** python -m SimpleHTTPServer 8080
	** Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.
    ** open a second terminal window
    ** cd /path/to/your-project-folder
    ** ngrok 8080
    ** Use the link it's display on the second terminal to access the website.

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html
	** Inline css recommended by PageSpeed in order to get more speed
	** Took out the font link, too heavy for the loading process.
	** CSS for media print was made.
	** Asyncronimous call for perfmatters.js and Google analytics.js 
	** All images were optimized using http://optimizilla.com/


####Part 2: Optimize Frames per Second in pizza.html
	** CSS files were minimized for better loading process.

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 
	** Resizes pizza function was optimized including the width selector within it's code for better performance.  Also using a % value for resizing.
	** Replaced the call for the document pizza container in order to use it within the for loop
	** Update position function optimized:  properties obtained by using getElementsByClassName.  Stored length of the object 'mover' and also the scrollTop propertie of the Document.
	** Variable 'phase' declared outside the loop.
	** The 'DOMContentLoaded' even listener optimized: variables declare outside the loop, number of pizzas to generate obtain outside the loop (tried with window.screen.height propertie but it didn't work well).
	** CSS files minimized.



	note: Browser caching, configured server-side, could have reduced page loading time.


