# Class 11

## Audio and Video

On the early days of the internet, there was a boom in audio and video content. These were largely enabled by plugin-based technologies such as Adobe Flash and Microsoft Silverlight. The issue was that both of these had many security and accessibility issues. Now, we have native HTML solutions, \<videos> and \<audio>, and JavaScript APIs to control them.

### \<video>

The \<video> element allows for the embedding of videos. To link a path to a specific video, we use the src attribute. The control attribute may be used to include the browser's own control interface. This will give the minimum requirement to grant the ability to pause the video or control its volume.

### \<audio>

The \<audio> element essentially works the exact same way as \<video>, just with a few key differences:

- \<audio> doesn't support width/height attributes as there is no visual component.
- Does not support the poster attribute for the same reason.

The differences between video and audio is simply that you can see video, but you have to believe audio. :think about it:

## Grid

Grid is a two-dimensional grid-based layout system that allows for precise positioning of elements. It is more annoying and complex than flex, but allows the creation of really cool looking websites.

### Terminology

Here is a list of Grid terms:

- Grid Container: The element which display: grid is applied. Should be the parent of all grid items.
- Grid Item: Direct children of the Grid. Born in a world of rigidity.
- Grid Line: The divisional lines that make up the Grid structure. They can be both vertical and horizontal.
- Grid Cell: The space between the lines. Contains hidden meanings.
- Grid Track: Essential rows or columns made of Grid cells.
- Grid Area: The space between four grid lines.

## Responsive Images

The concept of responsive images is the idea of images working well on a range of devices, screen sizes, resolutions, etc.  
We want responsive images so that our websites don't look great of computer screens but terrible on mobile devices.

### How to

In order to create responsive images, we need to first account for different screen sizes.  
The \<img> element has attributes that allow for this:

- srcset: Defines the set of images we give the browser to choose between, and the size of each image.
  - We set this by writing the image path along with the image's intended width.
  - > srcset='image-100w.jpg 100w'
- sizes: Defines the set of media conditions and indicates what image size would be best suited.
  - Contains a media conditions followed by the width of the slot the image will fill when true.
  - > media='(max-width: 600px)'

## Things I want to know more about
