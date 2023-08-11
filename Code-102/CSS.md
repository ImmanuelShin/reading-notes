# Design web pages with CSS

## CSS

Cascading Style Sheets (CSS), allows you to control, to a much greater degree than HTML, how documents are designed. From basic text styling, such as color or size, to page layouts, or even to animations, CSS gives you the ability to make your document look presentable.

### Syntax

CSS is a rule-based language where you define rules for specific groups of elements. These rules will control the styles that the specified group of elements will have.

> `h1 {`  
  `color: red;`  
  `font-size: 5em;`  
  `}`

- The above starts with a selector, in this case h1, that selects for the HTML element h1, or level one headings.
- Next, there are the open and closed curly braces to contain the rest of the rules.
- Inside the braces are the actual declarations, or rules:
  - `color` and `font-size` which are the properties of the declaration.
  - `red` and `5em` which are the values of the properties respectively.

### How to CSS

There are three ways to insert CSS into your project:

- External CSS: Externalize all of the stylings by moving them to a separate file.
  - > `<link rel="stylesheet" href="styles.css>`
  - Putting this in an html document will link up the document with the external "styles.css" file.
- Internal CSS: Typically used if a single HTML page has a separate unique style.
  - > `<!DOCTYPE html>`
    > `<html>`  
    > `<head>`  
    > `<style>`  
    > `body {`  
    > &nbsp;&nbsp;`background-color: linen;`  
    > `}`  
    >  
    > `h1 {`  
    > &nbsp;&nbsp;`color: maroon;`  
    > &nbsp;&nbsp;`margin-left: 40px;`  
    > `}`  
    > `</style>`  
    > `</head>`  
    > `<body>`  
    >  
    > `<h1>This is a heading</h1>`  
    > `<p>This is a paragraph.</p>`  
    >  
    > `</body>`  
    > `</html>`  
- Inline CSS: Used when uniquely styling just a single element.
  - > `<h1 style="color:blue;text-align:center;">This is a center-aligned blue heading</h1>`

#### Example

Let's say we wanted to set a CSS rule that set all `<p>` elements to have red text (completely random and unforced example).

You would do so by:

- > `p {`  
    &nbsp;&nbsp;`color: red;`  
    `}`  
- First adding the p selector.
- Then adding the curly braces.
- And finally, within the braces, adding the property: `color`, and the value: `red`
