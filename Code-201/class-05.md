# Class 05

## More HTML

### Images

Images in HTML are an important information medium. Pictures are eye catching and cool.  
In order to incorporate images into HTML, we use the \<img> attribute.  
As good as images are, though, there are those who sometimes can't see the pictures or are on devices or areas that can't load them. For those people, we use the alt attribute.  
> \<img src="aHotDog.png" alt="A picture of a hotdog">

The alt attribute allows us to add a text description incase the image doesn't load. We use the alt attribute to increase accessibility for people using screen readers, adding text for search engines, or people who have limit data transfer on mobile devices.

### Semantic Images

Now, creating containers for images along with their captions can be difficult to semantically tag. This is where the \<figure> and \<figcaption> elements come in. These elements are specifically used to contain figures and captions.

> \<figure>  
> &nbsp;&nbsp;\<img  
> &nbsp;&nbsp;&nbsp;&nbsp;src="hotdog.png"  
> &nbsp;&nbsp;&nbsp;&nbsp;alt="A picture of a delicious hotdog.">  
> &nbsp;&nbsp;\<figcaption>  
> &nbsp;&nbsp;&nbsp;&nbsp; A delicious hotdog.  
> &nbsp;&nbsp;\</figcaption>  
> \</figure>

### Image Types

Pictures aren't the only types of images out there. Sometimes, different image file types are needed for different situations:

- gif: Graphics Interchange Format - Good for simple images and animations.
  - Great for simplicity, compatibility, and low resource environments.
- svg: Scalable Vector Graphics - Good for shapes and icons that must be accurately drawn at different sizes.
  - Great for images that can be drawn and need to be drawn at different sizes.
- PNG: Portable Network Graphics: Provides lossless compression, higher color depths than gif while also being more efficient.
  - Great for screenshots or any image that needs to be precisely reproduced.

## More CSS

### Colors

Colors are an important aspect of CSS, and understanding how colors work in CSS is a necessity.  
In CSS, colors exist at different layers. The two main layers are going to be the foreground and background. Like their names suggest, the background colors exist behind the foreground and vise versa for foreground colors. Imagine a house wall: The wall's paint color is the background color, and any painting or live laugh love decoration is the foreground color.

Let's try an example: We want to change our friend's colorless blog site.  
We can:

- Add a background color with "background-color: somecolor;"
- Change the color of the text with "color: someothercolor;"
- Maybe add some more text decorations with "text-decoration-color: somecolor2;"
  - This will add color to any underline, strike-through, etc.

### Fonts

We can further decorate text by changing its font, and there are a lot of fonts.  
Fonts are great for adding personality, matching a certain aesthetic, or infuriating a generation by using comic sans.  
When choosing fonts, make sure to keep a few warnings in mind:

- Some fonts aren't available to all systems. Choosing fonts that are available to almost all operating systems, web safe fonts, are the way to go.
- Some fonts are really bad for reading. Make sure the font you choose is at least legible.
- Use multiple fonts in case one of your fonts is not available for a specific system. Supply a font stack.

To manipulate fonts, we have a few options available to us:

- font-size: Changes the font's size.
- font-weight: Changes the font's boldness.
- font-style: Changes the font's italicization

### Text Layout

We also have many ways to manipulate the overall layout of our text:

- text-align: Changes the alignment of text within the given box (i.e left align, center align).
- line-height: Changes the line spacing (i.e single space, double space, 9001% spaced).
- letter-spacing/word-spacing: Changes the spacing between individual letters and whole words.

## Things I want to know more about

If we got giant mirrors, magically placed them extremely far out in the universe, and pointed them back towards us, would we eventually get images of prehistoric Earth?
