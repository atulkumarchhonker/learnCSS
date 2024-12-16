## &#9873; CSS Filters
This properties is used to apply the various effects to the elements for differentiate or make them match to the theme. 

### &#9780; Overview:
1. [Blur](#-blur)
2. [Brightness](#-brightness)
3. [Contrast](#-contrast)
4. [Grayscale](#-grayscale)
5. [Hue-rotate](#-hue-rotate)
6. [Invert](#-invert)
7. [Opacity](#-opacity)
8. [Sepia](#-sepia)
9. [Multiple Filters Effect](#multiple-filters-effect)

### &#10022; Blur:
It applies a Gaussian blur effect to an element.

*Syntax: `filter: blur(radius);`*

*Example:*
```css
.blurred-image {
  filter: blur(5px);
}
```

### &#10022; Brightness:
It adjusts the brightness of an element.

*Syntax: `filter: brightness(percentage);`*

*Example:*
```css
.brighter-image {
  filter: brightness(120%);
}
```

### &#10022; Contrast:
It adjusts the contrast of an element.

*Syntax: `filter: contrast(percentage);`*

*Example:*
```css
.higher-contrast-image {
  filter: contrast(150%);
}
```

### &#10022; Grayscale:
It converts an element to grayscale.

*Syntax: `filter: grayscale(percentage);`*

*Example:*
```css
.grayscale-image {
  filter: grayscale(100%);
}
```

### &#10022; Hue-Rotate:
It rotates the hue of an element.

*Syntax: `filter: hue-rotate(angle);`*

*Example:*
```css
.hue-rotated-image {
  filter: hue-rotate(90deg);
}
```

### &#10022; Invert:
It inverts the colors of an element

*Syntax: `filter: invert(percentage);`*

*Example:*
```css
.inverted-image {
  filter: invert(100%);
}
```

### &#10022; Opacity:
It sets the opacity of an element.

*Syntax: `filter: opacity(percentage);`*

*Example:*
```css
.transparent-element {
  filter: opacity(50%);
}
```

### &#10022; Sepia:
It applies a sepia tone to an element.

*Syntax: `filter: sepia(percentage);`*

*Example:*
```css
.sepia-image {
  filter: sepia(100%);
}
```

### &#10022; Multiple Filters Effect:
It apply the multiple filters to an element. By using the filter property separated by spaces.

Example:
```css
.filtered-image {
  filter: blur(5px) brightness(120%) contrast(150%);
}
```

---
[&#8682; To Top](#-css-filters)

[&#10094; Previous Topic](../docs/css-transitions.md) &emsp; [Next Topic &#10095;](../docs/css-clip-path.md)

[&#8962; Goto Home Page](../README.md)
