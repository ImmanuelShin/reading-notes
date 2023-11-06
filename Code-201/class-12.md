# Class 12

## \<canvas>

Allows you to draw 2D graphics using JavaScript.  
It requires at least two attributes to specify the size:

- width="someWidth"
- height="someHeight"

These attributes can be accessed via DOM methods:

> canvas.width = someWidth;  
> canvas.height= someHeight;

Due to its slightly newer standardization, \<canvas> requires a closing tag \</canvas> in order to display fallback content:

> \<canvas width="10" height="10" id="canvas">Message incase browser doesn't support canvas\</canvas>

\<canvas> also features the getContext() method that returns a render context object.  
It takes one argument that represents the type of context:

> let canvas = document.querySelector('#canvas');  
> let ctx = main.getContext('2d');  

[source](https://www.javascripttutorial.net/web-apis/javascript-canvas/)

## Chart.js

A popular library used to make charts in JavaScript. This library provides a collection of of chart types, plugins, and customization objects that are all frequently used/needed. It also allows for the use of many community-maintained chart types. Furthermore, it makes possible the combining of several chart types into a mixed chart. It is highly customizable and this is not a sponsored message.

Some of the included chart types are:

- Area chart
- Bar chart
- Bubble chart
- Line chart
- Scatter chart
- Pie/Doughnut charts

### Utilizing Chart.js

Using libraries like Chart.js is beneficial due to the fact that native JavaScript tables don't look as nice. Charts look nicer, they are easier to read, and they convey data much quicker than simple tables. The only issue is that they aren't they easiest to create. This is why Chart.js is so useful: it removes the hassle of creating these charts from scratch.

These charts could have been used to great effect in the Salmon Cookies assignment in order to display the sales tables much better.

## Things I want to know more about
