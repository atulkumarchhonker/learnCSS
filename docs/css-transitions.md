## &#9873; CSS Transitions
This properties is important to show the immediate changes on the elements at each time.

*Transitions will reflect on basis of changes in the element. But [CSS animations](./css-animations.md) are slightly different than Transitions by changing the style in the sequence order.*

### &#9780; Overview:
1. [Transition properties](#-transition-properties)
2. [Transition duration](#-transition-duration)
3. [Transition timing functions](#-transition-timing-functions)
4. [Transition delay](#-transition-delay)
5. [Shorthand Transition Property](#-shorthand-transition-property)
6. [Resize Property](#-resize-property)

### &#10022; Transition Properties:
It specify which properties should transition when their values get change.

*Syntax: `transition-property: property1, property2, ...;`*

*Example:*
```css
div {
  transition-property: background-color, transform;
}
```

### &#10022; Transition Duration:
It sets the duration of the transition.

*Syntax: `transition-duration: value;`*

*Example:*
```css
div {
  transition-duration: 0.5s;
}
```

### &#10022; Transition Timing Functions:
It defines the speed curve of the transition.

*Syntax: `transition-timing-function: value;`*

*Example:*
```css
div {
  transition-timing-function: ease-in-out;
}
```

### &#10022; Transition Delay:
It sets the delay before the transition starts.

*Syntax: `transition-delay: value;`*

*Example:*
```css
div {
  transition-delay: 1s;
}
```

### &#10022; Shorthand Transition Property:
It specifies all properties for the transition of the element.

*Syntax: `transition: property duration timing-function delay;`*

```css
transition: background-color 0.5s ease-in-out 1s;
```

### &#10022; Resize Property:
It allows the user to resize the element. It can be resized `vertical`, `horizontal` or `both`.

*Syntax: `resize: axis-value;`*

```css
resize: both;
```

---
[&#8682; To Top](#-css-transitions)

[&#10094; Previous Topic](../docs/css-animations.md) &emsp; [Next Topic &#10095;](../docs/css-filters.md)

[&#8962; Goto Home Page](../README.md)
