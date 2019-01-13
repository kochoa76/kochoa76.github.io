---
layout: post
title:      "Front-End Development Review"
date:       2019-01-13 17:20:23 +0000
permalink:  front-end_development_review
---

I recently had an interview focused mainly on front-end languages like HTML/CSS and Javascript. I'm very grateful for the experience and really enjoyed meeting the team. 

While preparing for the interview I started reviewing a few of these languages and found a few pieces regarding HTML/CSS  I wanted to brush up on. 

**What is a polyfill? **

A polyfill is a browser fallback, made in JavaScript, that allows functionality you expect to work in modern browsers to work in older browsers. For example, many previous versions don't support HTML5 features, a polyfill would resolve this issue. 

JavaScript is the language used to create a polyfill, but a polyfill can be used to implement various browser features other than ES5, ES6 standards such as: 

SVG
Canvas
Web Storage (local storage / session storage)
Video
Cross-Origin Resource Sharing (CORS)
HTML5 elements
CSS responsive design modules
Accessibility / ARIA
Web Sockets
Geo Location
Browser State Management

**How do you target something inside or around another element?**
Remembering to target selectors and elements was something I could use some brushing up on. 

If you only want those that are direct children of the .nav specified to the left of the > then you can use the following syntax: 
```
.nav > .nav-item { ... }
```
You can also target all buttons that are next to another button this way: 
```
.button + .button { ... }
```

**What are pseudo elements and what are they used for?**
Pseudo elements are used to style particular parts of an element. You can use a pseudo element to style the first line or first letter of a paragraph, text you’ve selected, or you can use it to insert text or shapes before or after an element.

```
p::first-line { ... }
span::first-letter { ... }
::selection { ... }
.header::after { ... }
.tooltip::before { ... }

```
**What are pseudo classes and what are they used for?**
Pseudo classes are similar to pseudo elements, but instead of styling a part of an element, they apply styles when an element is in a certain state. An example would be applying the pseudo class :hover to an element so that when you hover over that particular element the style changes. 

Another common use case is to style the first p of your document, you could use the pseudo class `first-of-type`. 
They all start with a single colon and look like this:
```
.link:hover { ... }
.link:active { ... }
.tab:first-child { ... }
.tab:last-child { ... }
p:first-of-type { ... }

```

**Can you describe the rules around specificity?**
In using CSS you have the option of using tag/type selectors, class selectors or id selectors. Each has their own level of specificity. 

This means that if you add a style to either of the selectors above each one has their own level of priority(or specificity) to keep in mind: 

#ids - have highest priority and there is only to be one of that type of id `<div id="highest-priority></div>`
.class - have next level priority and there are usually a handful of class selectors `<div class="high-priority"></div>`
type selectors and/or pseudo-elements - have lowest specificity `<div></div>`

You can also increase an attributes specificity by adding ` !important ` to the css for ex. `font-family: Arial !important`
It's not recommended to use this feature frequently as it will get hard to keep track of the level of specificity for each attribute.

**The CSS Box Model**
 **How do margin, border and padding fit together in the box model?**
WIthin the box model you have border, padding, and margin. Border adds a border to whatever element you are targeting and margin and padding add spacing to that element. 

![](https://s3.amazonaws.com/viking_education/web_development/web_app_eng/css_box_model_chrome.png)

Padding targets the space between the element and the border while margin targets the space between the border and anything outside the element. It can be tricky at times to differentiate between padding and margin. 


**Flexbox vs CSS Grid **

Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces. It's important to keep in mind when you're using flexbox to add `display: flex` to the parent element of whatever it is you are looking to align as that will make a difference on whether you see any changes to the alignment. 

CSS Grid is a two-dimensional layout system for the web. It lets you lay content out in rows and columns, and has many features that make building complex layouts straightforward. It is a better method to use when looking to create a 'grid' like template on an entire page as it takes horizontal and vertical axes. 

**CSS preprocessors**
 CSS preprocessors are encouraged to use for larger projects as they provide a few benefits: 
 
 -Cleaner code with reusable pieces and variables
 -Saves you time
 -Easier to maintain code with snippets and libraries
 -Calculations and logic
 -More organized and easy to setup
 
The main players are Sass (also referred to as SCSS) and LESS 

SASS requires Ruby while LESS requires Javascript or Node.js  

