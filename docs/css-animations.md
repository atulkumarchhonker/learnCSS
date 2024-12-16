## &#9873; CSS Animations
It is used to create sequential order of change in the style of an element as an CSS animation.

### &#9780; Overview:
1. [Keyframes](#-keyframes)
2. [Animation properties](#-animation-properties)
3. [Animation timing functions](#-animation-timing-functions)
4. [Animation delay](#-animation-delay)
5. [Animation iteration count](#-animation-iteration-count)
6. [Animation direction](#-animation-direction)

### &#10022; Keyframes:
It define the specific points in an animation sequence.

*Syntax: `@keyframes animation-name { ... }`*

*Example:*
```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

```css
@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
```

```css
@keyframes fade-in {
  0%, 100% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}
```

```css
@keyframes fade-in {
  to {
    opacity: 1;
  }
}
```

### &#10022; Animation Properties:
This defines set of properties for handling and control how an animation is played.

*Syntax: `animation: animation-name animation-duration animation-timing-function animation-delay animation-iteration-count animation-direction;`*

*Example:*
```css
div {
  animation: fade-in 2s ease-in-out 1s infinite alternate;
}
```

### &#10022; Animation Timing Functions:
It defines the speed curve of the animation.

*Syntax: `animation-timing-function: value;`*

*Example:*
```css
animation-timing-function: ease-in-out;
```

### &#10022; Animation Duration:
It sets the length of the animation.

*Syntax: `animation-duration: value;`*

*Example:*
```css
animation-duration: 3s;
```

### &#10022; Animation Delay:
It sets the delay before the animation starts.

*Syntax: `animation-delay: value;`*

*Example:*
```css
animation-delay: 1s;
```

### &#10022; Animation Iteration Count:
It sets the number of times the animation should play.

*Syntax: `animation-iteration-count: value;`*

*Example:*
```css
animation-iteration-count: 3;
```

### &#10022; Animation Direction:
It sets the direction of the animation playing state.

*Syntax: `animation-direction: value;`*

*Example:*
```css
animation-direction: alternate;
```

---
[&#8682; To Top](#-css-animations)

[&#10094; Previous Topic](../docs/responsive-design.md) &emsp; [Next Topic &#10095;](../docs/css-transitions.md)

[&#8962; Goto Home Page](../README.md)
