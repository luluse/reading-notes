# CSS Transforms, Transitions, and Animations

## Transform

> The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

2D Transoforms:
- `transform: rotate(20deg);` from 0 to 360 degrees. Positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise
- `transform: scale(.75);` It is possible to scale only the height or width of an element using the scaleX(width) and scaleY(height) values.
- `transform: translate(-10px, 25%)` works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document. translateX (horizontal), translateY (vertical).
- `transform: skew(5deg, -20deg);` is used to distort elements on the horizontal axis, vertical axis, or both.

To combine transforms, list the transform values within the transform property one after the other without the use of commas.

Perspective:
- In order for three-dimensional transforms to work the elements need a perspective from which to transform.
- `transform: perspective(200px) rotateX(45deg);`

3D Transforms:

we use three new transform values, including rotateX, rotateY, and rotateZ.
- `transform: perspective(200px) scaleZ(1.75) rotateX(45deg);`
- Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale. 
- `backface-visibility: hidden;`will hide the element whenever it is facing away from the screen

## Transitions

for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the **:hover, :focus, :active, and :target** pseudo-classes.

- `transition-property`determines exactly what properties will be altered in conjunction with the other transitional properties

> not all properties may be transitioned


- `transition-duration` duration in which a transition takes place
- `transition-timing-function` used to set the speed in which a transition will move.
- `transition-delay` determines how long a transition should be stalled before executing.

## Animations

To set multiple points at which an element should undergo a transition, use the **@keyframes** rule. The **@keyframes** rule includes the animation name, any animation breakpoints, and the properties intended to be animated.
```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```
Once the keyframes for an animation have been declared they need to be assigned to an element:
- the animation-name property is used with the animation name
```
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
}
```
- `animation-iteration-count` repeat itself numerous times
- `animation-direction` property include normal, reverse, alternate(play an animation forwards then backwards), and alternate-reverse.