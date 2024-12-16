## &#9873; Properties and Values
For applying specific CSS styles to the element, there is certain properties exist on each and every element of the HTML.

### &#10022; Understanding Properties:
The element properties are attributes that define the style of an HTML element. They determine how elements look and behave on a webpage.

### &#10022; Setting Values:
The values are assigned to properties to specify the desired style. They can be:

- Keywords: Predefined values like `inherit`, `initial`, `unset`, `revert`, `revert-layer`.
- Numbers: `Numerical values`, often with units.
- Units: Used with numbers to specify measurements, like `px`, `em`, `rem`, `%`, `vh`, `vw`.
- Colors: Specified using `color names`, `hex codes`, `RGB values`, `HSL values`, etc.
- Functions: Built-in functions that perform calculations or manipulations on values such as `calc()`.

*There are almost 12 common properties in CSS.*

### &#9780; Overview:
1. [color](#-color)
2. [background](#-background)
3. [font](#-font)
4. [margin](#-margin)
5. [padding](#-padding)
6. [border](#-border)
7. [display](#-display)
8. [position](#-position)
9. [float](#-float)
10. [width](#-width)
11. [height](#-height)
12. [overflow](#-overflow)

### &#10022; Color:
It sets the color of the text.

*Syntax: `color: value;`*

```css
p {
  color: blue;
}
```
### &#10022; Background:
It sets the background style of an element.

*Syntax: `background: value;`*

```css
div {
  background-color: #f0f0f0;
  background-image: url("image.jpg");
  background-repeat: no-repeat;
  background-position: center;
}
```
### &#10022; Font:
It sets the font family, size, style, and weight.

*Syntax: `font: value;`*

```css
h1 {
  font: 24px Arial, sans-serif;
  font-weight: bold;
  font-style: italic;
}
```
### &#10022; Margin:
It sets the space outside an element.

*Syntax: `margin: value;` or `margin: top-bottom left-right;` or `margin: top right bottom left;`*

Or it sets margin value to individual side.

*Syntax: `margin-top: value;`, `margin-right: value;`, `margin-bottom: value;`, `margin-left: value;`*

```css
p {
  margin: 10px;
}

h3 {
  margin: 5px 10px;
}

span {
  margin: 10px 5px 10px 5px;
}
```
### &#10022; Padding:
It sets the space inside an element.

*Syntax: `padding: value;` or `padding: top-bottom left-right;` or `padding: top right bottom left;`*

Or it sets padding value to individual side.

*Syntax: `padding-top: value;`, `padding-right: value;`, `padding-bottom: value;`, `padding-left: value;`*

```css
p {
  padding: 10px;
}

h3 {
  padding: 5px 10px;
}

span {
  padding: 10px 5px 10px 5px;
}
```
### &#10022; Border:
It creates a border around an element.

*Syntax: `border: value;` or `border: width style color;`*

Or it sets border to individual side.

*Syntax: `border-top: value;`, `border-right: value;`, `border-bottom: value;`, `border-left: value;`*

```css
button {
  border: 2px solid blue;
}
```
### &#10022; Display:
It sets the display type of an element.

*Syntax: `display: value;`*

```css
.hidden {
  display: none;
}
```
### &#10022; Position:
It sets the positioning of an element.

*Syntax: `position: value;`*

```css
.fixed-element {
  position: fixed;
  top: 0;
  right: 0;
}
```
### &#10022; Float:
It floats an element to the left or right.

*Syntax: `float: value;`*

```css
img {
  float: left;
}
```
### &#10022; Width:
It sets the width of an element.

*Syntax: `width: value;`*

```css
div {
  width: 500px;
}
```
### &#10022; Height:
It sets the height of an element.

*Syntax: `height: value;`*

```css
img {
  height: 200px;
}
```
### &#10022; Overflow:
It specifies how content is handled if it overflows the element's box.

*Syntax: `overflow: value;`*

```css
div {
  overflow: hidden;
}
```

---
[&#8682; To Top](#-properties-and-values)

[&#10094; Previous Topic](./selectors.md) &emsp; [Next Topic &#10095;](./css-units.md)

[&#8962; Goto Home Page](../README.md)
