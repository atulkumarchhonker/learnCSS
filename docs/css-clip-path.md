## &#9873; CSS Clip Path

CSS clip path is a property that allows to customize a shape by masking or clipping the content of an element. This means that only the portion of the content of the element that falls within the specified shape will be visible.

### &#9780; Overview:
1. [Basic Clip Path:](#-basic-clip-path)
	- [Common shape functions](#-common-shape-functions)
		- [circle](#-circle)
		- [ellipse](#-ellipse)
		- [polygon](#-polygon)
		- [inset](#-inset)
2. [Advanced Clip Path:](#-advanced-clip-path)
	- [Path Function](#-path-function)
	- [URL Function](#-url-function)
3. [Clip Rule property](#-clip-rule-property)
    - [nonzero](#-nonzero)
    - [evenodd](#-evenodd)
4. [Use Cases and Examples:](#-use-cases-and-examples)
	- [Creating custom shapes](#-creating-custom-shapes)
	- [Masking elements](#-masking-elements)
	- [Creating unique visual effects](#-creating-unique-visual-effects)
	- [Combining with other CSS properties](#-combining-with-other-css-properties)

### &#10022; Basic Clip Path:

### &#10022; Common Shape Functions:
The clip path property can create common shapes with available function such as circle, ellipse, polygon.

### &#10022; Circle:
It allows to define a circle that masks or clips the content of an element.

*Syntax:*
```css
clip-path: circle(radius at center-x center-y);
```
- radius: Specifies the radius of the circle.
- center-x: Specifies the x-coordinate of the circle's center.
- center-y: Specifies the y-coordinate of the circle's center.
- *Note:* If the center-x and center-y part are not mentioned, the center of the circle defaults to the center of the element.

```html
<div class="circle"></div>
```

```css
.circle {
  width: 100px;
  height: 100px;
  background-color: blue;
  clip-path: circle(50% at 50% 50%);
}
```

### &#10022; Ellipse:
It allows to define an ellipse that masks or clips the content of an element.

*Syntax:*
```css
clip-path: ellipse(radius-x radius-y at center-x center-y);
```
- radius-x: Specifies the horizontal radius of the ellipse.
- radius-y: Specifies the vertical radius of the ellipse.
- center-x: Specifies the x-coordinate of the ellipse's center.
- center-y: Specifies the y-coordinate of the ellipse's center.
- *Note:* If the center-x and center-y part are not mentioned, the center of the ellipse defaults to the center of the element.

```html
<div class="ellipse"></div>
```

```css
.ellipse {
  width: 200px;
  height: 100px;
  background-color: green;
  clip-path: ellipse(50% 25% at 50% 50%);
}
```

### &#10022; Polygon:
It allows to define a polygon with number of connected points to frame a shape that masks or clips the content of an element. 

*Minimum polygon forms a triangle with three point connected with each other. And increasing in these points forms a different polygons.*

*Syntax:*
```css
clip-path: polygon(point1, point2, ...);
```

*Note: Coordinates of the points are specified in the format of x y.*

```html
<div class="triangle"></div>
```

```css
.triangle {
  width: 100px;
  height: 100px;
  background-color: red;
  clip-path: polygon(0% 0%, 100% 0%, 50% 100%);
}
```
- The clip-path property creates a triangle by specifying three points:
	- The top-left corner (0% 0%)
	- The top-right corner (100% 0%)
	- The bottom-center (50% 100%)

### &#10022; Inset:
It creates an inset shape.

*Syntax:*
```css
clip-path: inset(top right bottom left);
```
- top: Specifies the inset distance from the top edge.
- right: Specifies the inset distance from the right edge.
- bottom: Specifies the inset distance from the bottom edge.
- left: Specifies the inset distance from the left edge.
*Note: All values can be specified in various units, such as pixels (px), percentages (%), or ems.*

```html
<div class="inset"></div>
```

```css
.inset {
  width: 200px;
  height: 100px;
  background-color: yellow;
  clip-path: inset(20px 30px 40px 50px);
}
```

- The clip-path property creates an inset shape that cuts away,
	- 20 pixels from the top, 
	- 30 pixels from the right, 
	- 40 pixels from the bottom, 
	- 50 pixels from the left of the element.

- *Negative Values:* Using negative values for the inset distances can create outward-facing shapes.
- *Rounded Corners:* To create rounded corners for the inset shape, you can use the border-radius property on the element.

### &#10022; Advanced Clip Path:

### &#10022; Path Function:
Path data strings are a powerful way to define complex shapes in SVG. They consist of a series of commands and coordinates that describe the path's outline.

- Common Path Commands:
	- M: Moveto: Sets the starting point of the path.
	- L: Lineto: Draws a straight line to the specified point.
	- C: Curveto: Draws a cubic Bezier curve to the specified point.
	- S: Smooth curveto: Draws a cubic Bezier curve to the specified point, using the reflection of the previous curve's control point.
	- Q: Quadratic Bezier curveto: Draws a quadratic Bezier curve to the specified point.
	- T: Smooth quadratic Bezier curveto: Draws a quadratic Bezier curve to the specified point, using the reflection of the previous curve's control point.
	- A: Arc: Draws an elliptical arc to the specified point.
	- Z: Closepath: Closes the current path by drawing a straight line from the current point to the starting point.

*Example for creating rectangle:*
`
M 50 50
L 100 0
C 150 0 200 50 200 100
L 200 200
L 50 200
Z
`

*Syntax:*
```css
clip-path: path(path-data-string);
```

```html
<div class="custom-shape"></div>
```

```css
.custom-shape {
  width: 200px;
  height: 200px;
  background-color: blue;
  clip-path: path(M 50 50 L 100 0 C 150 0 200 50 200 100 L 200 200 L 50 200 Z);
}
```

### &#10022; URL Function:
It allows to define shapes using path data strings or directly referencing SVG paths. The url() function is used to reference an SVG file containing the desired shape.

*Syntax:*
```css
clip-path: url(url-to-svg-file);
```

```html
<div class="custom-shape"></div>
```

```css
.custom-shape {
  width: 200px;
  height: 200px;
  background-color: blue;
  clip-path: url(shape.svg);
}
```

### &#10022; Clip Rule property:
The clip-rule property in CSS determines how the clipping region is filled when using complex shapes with overlapping paths. It affects whether points inside or outside the shape are included in the clipped region.

### &#10022; Nonzero:
This is the default rule. It uses the non-zero winding rule to determine whether a point is inside or outside a shape. The rule calculates the number of times a ray emanating from the point intersects the shape's outline. If the number is odd, the point is inside; if it's even, the point is outside.

```css
clip-path: polygon(0% 0%, 100% 0%, 50% 100%);
clip-rule: nonzero;
```

*In this case, the triangle will be filled completely, even if there are overlapping paths within the shape.*

### &#10022; Evenodd:
This rule uses the even-odd fill rule to determine whether a point is inside or outside a shape. It counts the number of times a ray emanating from the point intersects the shape's outline. If the number is even, the point is inside; if it's odd, the point is outside.

```css
clip-path: polygon(0% 0%, 100% 0%, 50% 100%, 50% 50%);
clip-rule: evenodd;
```

*In this case, the triangle will have a hole in the middle because the overlapping path (the line from 50% 50% to 50% 100%) creates an additional contour.*

### &#10022; When to Use Which Rule:
- `nonzero`: Use this rule when you want to fill the entire shape, even if there are overlapping paths.
- `evenodd`: Use this rule when you want to create more complex shapes with holes or cutouts.

### &#10022; Additional Notes:
- The clip-rule property is supported by most modern web browsers.
- To combine the clip-rule property with other CSS properties like clip-path to create intricate visual effects.

### &#10022; Use Cases and Examples:

### &#10022; Creating custom shapes:
- Creating Circle:
```css
.circle {
  clip-path: circle(50% at 50% 50%);
}
```

- Polygonal elements:
```css
.triangle {
  clip-path: polygon(0% 0%, 100% 0%, 50% 100%);
}
```

### &#10022; Masking elements:
- Revealing a portion of an image:
```css
.masked-image {
  clip-path: circle(50% at 50% 50%);
}
```

- Hiding a portion of text:
```css
.masked-text {
  clip-path: polygon(0% 0%, 100% 0%, 100% 50%, 0% 50%);
}
```

### &#10022; Creating unique visual effects:
- Pulsating shapes:
```css
.pulsating-circle {
  clip-path: circle(50% at 50% 50%);
  animation: pulse 2s infinite;
}
```

- Revealing content:
```css
.revealing-content {
  clip-path: circle(0% at 50% 50%);
  animation: reveal 1s ease-in-out forwards;
}
```

- Creating custom transitions:
```css
.transitioning-element {
  clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%);
  transition: clip-path 0.5s ease-in-out;
}
```

### &#10022; Combining with other CSS properties:
- Transforming shapes:
```css
.transformed-shape {
  clip-path: circle(50% at 50% 50%);
  transform: rotate(45deg);
}
```

- Animating shapes:
```css
.animated-shape {
  clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%);
  animation: shape-change 2s infinite;
}
```

---
[&#8682; To Top](#-css-clip-path)

[&#10094; Previous Topic](../docs/css-filters.md)

[&#8962; Goto Home Page](../README.md)