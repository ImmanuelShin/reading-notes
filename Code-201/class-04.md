# Class 04

## HTML Continued

### Hyperlinks

Links are important to any website. They are important to linking your webpage to anywhere: other sites, documents, resources, etc. Imagine a news site without any links, it be like reading a newspaper, terrible.

To create these useful links, you need to use an \<a> element alongside a href attribute:
> \<a href="https://www.website.com">The text shown on your hyperlink\</a>  

The href attribute will be the key part holding your url's address.  

To make sure links are accessible to all, we need to keep a few things in mind:

- Include keywords from search engines.
- Make sure links are made of actual text descriptions instead of the URL itself.
- Make sure the descriptions aren't too long.
- Try not to have the same link pop up multiple times.

## CSS Continued

### Normal Flow

Normal flow is the default way that elements on a webpage are laid out. As long as there is no change or removal of CSS, the HTML site will look a normal flow way. It serves as a decent starting point in making your website look better rather than starting from nothing.

Referring back to the box model, there are two types of elements that act different within this model:

- Block-level elements: Fills up the space given to it by its parent. Imagine taking up all the space within a room of your parent's house.
- inline-level elements: Fills only to the size of its own content. Imagine just being yourself inside an empty room of your parent's house.

### Positioning

While normal flow is a nice starter guide, often times we will want to change up how the website looks and is laid out. Positioning allows us to do so. It overrides normal flow to put chosen objects to wherever our hearts desire.

- Static: The default for every HTML element. Applying this just means "use default settings" basically.
- Relative: Allows the object to be moved relative to its normal position. Using top, left, bottom, right attributes allows you to push the object from that direction (i.e top: 30px; means to push the box from the top, downwards 30px).
- Absolute: Different to relative, instead of starting from the normal position, we describe exactly where we want the object to be from its first positioned parent. Imaging being inside a house. The house is your first positioned parent. Positioning yourself absolutely to it at, say, top: 30px, left: 30px, we'd be 30px from the top of the house and 30px from the left side of the house.
  - Absolute has the advantage of being separated from the default flow. As it sits on its own layer, this creates an isolated element that doesn't interfere with the overall layout of the page.
- Fixed: Similar to absolute, instead of being absolutely fixed to a parent, it is absolutely fixed to the overall viewable screen. Imagine a navigation menu on either the side or top of the page. It will normally always stay in view no matter how much we scroll. That is fixed positioning.

## JS Continued

### Functions

Quick overview, functions are blocks of reusable code. In order to create it, we first declare it by creating it:
> function myFunction() {  
>
> }

In order to invoke it, or call it, we can simply call its name followed by the parenthesis:
> myFunction();

Now sometimes we need to pass values into the function, say if we want the function to return something based on the values passed to it:
> function myFunction(param1, param2) {  
>
> }

In this function, we set a few parameters to act as the variables for what values will be passed to it.  
When calling the function, we need to include all the arguments needed by the parameters:
> myFunction(arg1, arg2);

## Pair Programming

Pair programming is literally rally car racing with less steps and less danger. There is a driver that types code and a navigator that directs the driver. This creates a team effort that can enhance or quicken the coding process.  
What's really great about it is that it is extremely efficient. Instead of having to path find while walking, you get to either just focus on walking, or focus on path finding. This creates a greater quality between both sides as they are each allowed to focus on just one thing.
What's also great is that it allows two people to bounce ideas off each other without the fogginess of not knowing what each other person is doing. Collaboration is awesome when both parties are in full knowledge of the target subject. Also, it allows for one person to not have to type. That's sick.

## Things I want to know more about

Instead of resurrecting old dinosaurs, I wonder if we could influence a certain species' evolution to become the common ancestor to a whole new breed of dinosaurs.