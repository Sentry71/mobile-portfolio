## Website Performance Optimization portfolio project

For this project, a web portfolio was provided, which requires some modification to work optimally. The objective of this project is to optimize that portfolio, using skills obtained from the [Website Perfomance Optimization](https://www.udacity.com/course/ud884 "Udacity Course UD884" ) course on Udacity.

### How to Test
1. For the PageSpeed Insights Score, open the [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) link and copy the URL to be tested into the space provided, and click the Analyze button.
  * URL: http://sentry71.github.io/mobile-portfolio/index.html
2. For the Frames Per Second reading, open the below URL in Chrome. Navigate to the DevTools page (menu > View > Developer > Developer Tools). Click on the Timeline tab. Record a trace, and verify the Frames mode is on (looks like a set of vertical bars).
  * URL: http://sentry71.github.io/mobile-portfolio/views/pizza.html


### Steps Taken to Improve PageSpeed Score
* Moved required CSS for first render into a style tag on the HTML page
* Optimized images using [ImageOptim](https://imageoptim.com) for Mac
* Added "async" attribute on the JavaScript script tags, to load data asynchronously
* These modifications allowed the Google PageSpeed Insights scores to be above 90 on both desktop and mobile


### Steps Taken to Improve Frames per Second
* Moved entire style.css file into HTML page for first render
* Minified CSS and JavaScript files (both regular and minfied versions are in their respective /views/css and /views/js folders)
* Optimized images using [ImageOptim](https://imageoptim.com) for Mac
* Made several changes to main.js, in order to optimize frame rate
  * Moved sizeSwitcher() function (line 426) outside of the function it was defined in (line 441)
  * Moved static values outside the "for" loop in changePizzaSizes() function (line 455-457), the "pizza append on page load" function (line 476) and updatePositions() function (line 511-512)
* By making these modifications, the frame rate should be consistently above 60fps when measured using Chrome DevTools

All final code can be viewed at the repository where this README is located.

#### References Used
* igvita.com - Ilya Grigorik
https://www.igvita.com/2012/09/12/web-fonts-performance-making-pretty-fast/
* essential CSS in style tag
https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery
* ImageOptim - image optimization tool
https://imageoptim.com
* CSS minifier
http://csscompressor.com
* JS minifier
http://jscompress.com
