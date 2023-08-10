# Structure web pages with HTML

## What is HTML?

HTML, or HyperText Markup Language, is a coding language that is used to structure web pages. It consists of a series of elements that allow you to format the contents of the web pages in certain ways.

### HTML Elements

#### Element Structure

There are three parts to an HTML element:

1. Opening tag:
    - Contains the name of the element enclosed in angle brackets.
    - > `<element>`
2. Content:
    - Any content to be contained within the element.
3. Closing tag:
    - Same as the opening tag, but with a forward slash before the element name.
    - > `</element>`

All together, the element will look like this:

- > `<element> Cool Content bro </element>`

#### Attributes

Sometimes elements will contain additional information, or attributes, that give the element additional characteristics.

- > `<element class="extra-info">Content</element>`

In this case, the `class` attribute is giving the element the `extra-info` value.

While not every attribute will have a value, those that do will always have:

1. A space between it and the element name.
2. The attribute name followed by an equal sign.
3. The attribute value wrapped by opening and closing quotation marks.

#### Semantics

The *meaning* of a piece of code. In HTML, various elements will be semantic elements, which gives the content the element wraps with a specific role.

The semantic element h1, for example, gives the text it wraps the role of a top level header.

- > `<h1>This is a top level header</h1>`

##### Semantic Benefits

- Search engines consider its contents as important keywords to influence the page's search rankings.
- Screen readers can use them as signposts to help visually impaired users navigate pages.
- Makes code much more readable:
    - Gives a visual indication to the developer what type of data should be populated within.
    - Gives better visual structure to the lines of code.
