# Class 08

## CSS Layout

### Flexbox

Flexible Box Layout Model is a layout that is designed to be very flexible. It can take content of all sizes and make them work with each other. It provides an alternative to rigid layouts that can easily break on different viewing screens.  
Flexbox is designed for one dimensional content. This means that it only deals with layouts in a single direction, rows or columns.  
These are the features of flex layouts:

- They can display as a row, or a column.
- They respect the writing mode of the document.
- They are single line by default, but can be asked to wrap onto multiple lines.
- Items in the layout can be visually reordered, away from their order in the DOM.
- Space can be distributed inside the items, so they become bigger and smaller according to the space available in their parent.
- Space can be distributed around the items and flex lines in a wrapped layout, using the Box Alignment properties.
- The items themselves can be aligned on the cross axis.  
[source](https://web.dev/learn/css/flexbox/)

Considering flexbox deals in one dimension, our greatest control over flexbox comes from our understanding of its axes:

- Main Axis: The main axis is set by flex-direction. It can be either rows or columns.
  - flex-direction: Can be set to:
    - row: Items layout in a row.
    - row-reverse: Items layout in a row starting from the end.
    - column: Items layout in a column.
    - column-reverse: Items layout in a column starting from the end.
- Cross Axis: The axis that is opposite to the one set by flex-direction.

Take caution in using properties that reorder the visual display from the original HTML order. It can negatively impact accessibility. The logical order remains even if visually, they aren't, so screen readers will get mixed up.

### Why Flexbox?

It's easier.  
Long ago, in a land before time, dinosaurs walked the earth in very rigid and hard to maneuver lines. Vertically centering a div was almost impossible, equalizing width/heights amongst children despite available width/height was a nightmare, and making containers with different size content match height was downright inconvenient.

At the end of the day, just learn flexbox.

## Things I want to know more about
