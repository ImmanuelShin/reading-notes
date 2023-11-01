# Class 09

## HTML Forms

Web forms are some of the main interactive points between a user and a website. They allow the user to input data in order to update the information on the web page in some way.  
HTML forms are made up of controls and structure elements. The controls are made up of many different types of mainly input elements.  
Keep in mind that a simple and focused form is generally best for all users and applications.

### Implementing Forms

In order to create HTML forms, we will use a few elements:

- \<form>: Formally defines a form. It is a container element specifically for forms. Has two standard attributes:
  - Action: Defines the location where the collected data will be sent to.1
  - Method: Defines the HTTP method to send the data with.
- \<label>: Place to put name/label/description for the following input.
- \<input>: Input field. Certain attributes lets you define what type of inputs will be accepted.
- \<textarea>: Allows you to place a large area for users to type in.
- \<button>: Interactive element that performs an action upon activation.

## JS Events

Events are simply things that happen in the system. These events produce signals that can be captured and reacted to by other items.  
Some event examples:  

- The user selects, clicks, or hovers the cursor over a certain element.
- The user chooses a key on the keyboard.
- The user resizes or closes the browser window.
- A web page finishes loading.
- A form is submitted.
- A video is played, paused, or ends.
- An error occurs.  
[source](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

There are a few manual ways to handle certain events, such as buttons with onclick events in HTML. However, there is a more recommended mechanisms: addEventListener().

Basically all objects that have can send event signals have the addEventListener() method. When firing the event, we need two pass two parameters for the newly defined addEventListener() function:

- A string that indicates what type of event we want to listen to. Some examples:
  - "click" for click events.
  - "mouseover" for when the mouse is moved over our object.
- A function to call when the event happens. Can be anything.

### Event Object

Sometimes, we will use parameters named event, evt, e, etc. These are even objects and are automatically passed to event handlers to provide extra information. Event objects allow us to target the objects that created the event themselves, or keep track of what exactly happened and interact with it.

### Event Bubbling

Event bubbling is how the browser handles events targeted at nested elements.  
Take a button that is within a div element. We can attach a click event handler to the div, the parent, and have the parent fire the event signal. This works because if we click the button, we are also technically clicking the parent div.  
Now what it we add event handlers to not only the parent div, but to the button and the div's parent, let's say body, as well. This is where bubbling happens. Upon clicking the button, all three elements will fire a click event. We describe this occurrence by saying that the event bubbles up from the innermost element.  
This can be simultaneously both useful and harmful.

### Event Capturing

Essentially the same as event bubbling, just in the reverse order. This is disabled by default and must be enabled via the capture option in addEventListener().

We have both bubbling and capture because of two old browsers were unable to agree.

## Things I want to know more about
