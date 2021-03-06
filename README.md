<h1 align="center">Easy Scroll Dots :</h1>
<p align="center"><strong>Quickly add anchor points throughout your web page/application and have navigational dots automatically appear in a fixed position on the side of the page. This allows the user to click to scroll though sections of the page, and it updates as they scroll.</strong></p>
<p align="center"><em>Unlike some other plugins, Easy Scroll Dots does NOT require your web site or application to have a full page or full width slide design. Simply add your anchor points to any sections within your HTML and Easy Scroll Dots will do the rest.</em></p>
<p align="center"><img src="https://i.ibb.co/f4xMbHx/easy-Scroll-Dots-representation.jpg" alt="Easy Scroll Dots Representation" /></p>

# Browser/OS Support

<ul>
  <li><strong>Windows/Mac:</strong> Chrome &#10004; IE 11 &#10004; FF &#10004; Edge &#10004; Opera &#10004;</li>
  <li><strong>Android/IOS:</strong> Chrome &#10004; FF &#10004; Safari &#10004;</li>
</ul>
<p><em>Note: Easy Scroll Dots is vanilla and has no dependencies in order to work on Chrome and Firefox. However, jQuery is recommended if you need consistant and smooth animations across all of the supported browsers.</em></p> 

# Installation

## Including Files

```html
<!-- CSS for Easy Scroll Dots -->
<link rel="stylesheet" type="text/css" href="easyScrollDots.min.css" />

<!-- JS for Easy Scroll Dots -->
<script type="text/javascript" src="easyScrollDots.min.js"></script>
```

<p><em>Add the CSS file within your head tag, and add the JS file before the closing body tag. Update the paths depending on where you add the files within your project.</em></p>

## Usage

### Initialise

<p>Add the following function call somewhere in your javaScript AFTER the easyScrollDots.min.js file has been loaded...</p>

```javascript
easyScrollDots({
  'fixedNav': false,
  'fixedNavId': '',
  'fixedNavUpward': false
});
```

### Add your anchor points

<p>Add the folliwing HTML snippet at the start of each section of the page that should have a dot associated with it...</p>

```html
<div>
    <div class="scroll-indicator" id="section01" data-scroll-indicator-title="Hello World"></div>
</div>
```

<p><strong>Replace the id with something unique each time you add the snippet</strong>, and also update the data-scroll-indictaor-title to represent the title for that section of the page.</p>

<p><em>Remember, an id cannot have any spaces and cannot start with a number. Adding a unique id each time is required, and can be useful for creating deep link URLs to your content e.g. mysite.com/#section01</em></p>

## Options

<p>Some sites have a fixed or sticky top navigation bar which gets in the way when easyScrollDots scrolls the browser window to the top of each section. Therefore you have to tell easyScrollDots if you have a fixed nav, and if so, you also need to provide the id of the navigation bar. Finally you can also tell easyScrollDots if your fixed nav only appears when the user is scrolling upward.</p>

```javascript
easyScrollDots({
  'fixedNav': true, // Set to true if you have a fixed nav.
  'fixedNavId': 'myNav', // Set to the id of your navigation element (easyScrollDots will measure the height of the element).
  'fixedNavUpward': true // Set to true if your nav is only sticky when the user is scrolling up.
});
```

## Assumptions & Prerequisites

It is assumed that your application has a body tag. (easyScrollDots appends itself to the end of the body)

# Demo

<p>See a working demo on CodePen:</p>

<strong>https://codepen.io/SuperHands/pen/omqWBB</strong>

<p><em>The demo is using jQuery for full browser support, but jQuery is NOT required.</em></p>

## License

MIT - Free and unrestricted use.
