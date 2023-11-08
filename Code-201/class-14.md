# Class 14

## Transforms

The transforms property in CSS gives you alternatives to size, position, and change elements. The types of transformations come in two different settings: 2D and 3D.

### 2D Transformations

There are a multitude of transformations in the two-dimensional setting:

- 2D Rotate: Lets you rotate an element from 0 to 360 degrees.
  - Positive values will rotate clockwise, negative values vise versa.
- 2D Scale: Lets you change the apparent size of an element.
  - Default size is 1. scaleX and scaleY can be used to scale just one dimension.
- 2D Translate: Lets you move the apparent element away from its actual location.
  - Does not interrupt normal flow. translateX and translateY for each dimension. X comes first.
- 2D Skew: Lets you distort the element's appearance.
  - Uses degrees along either skewX or skewY axis.

The transform attribute is a useful tool, especially for cases where you want the appearance of an element to change without actually changing the overall normal flow of the webpage (i.e Making buttons "bounce" when hovered over).

## Transitions & Animations

CSS also gives you greater control over how elements look while changing or transforming with transitions and animations.

### Transitions

In order for transitions to work, the focus element must have gone through a change in state, and have different styles attached to each state. These states could be pseudo-classes such as :hover and :target. Transition allows you to make the change in state look meaningfully different.

There are four transition properties that you can employ:

- transition-property
- transition-duration
- transition-timing-function
- transition-delay

Not all of these are required, but you will find yourself using these quite often.

### Animations

Where transitions allow you to make a change in state look noticeable, animations allow you to set multiple transitions between states. This creates a smoother and more gradual change.

To set multiple points, @keyframes are used. Within the key frames, you can decide what changes at what point or time.

### Why You Should

Transitions and animations aren't simply there for fancy effects. Small transitions and simple animations go a long way in making a webpages look and feel more alive and responsive. Furthermore, when webpage don't react to our changes, the first thoughts that come to our heads is that the page is either very slow, very old, or something went wrong and the webpage just froze (i.e A button not highlighting itself when hovered over). Transitions and animations thus should be seen as required on any modern website.

## Things I want to know more about
