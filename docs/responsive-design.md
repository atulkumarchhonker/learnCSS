## &#9873; Responsive Design
These properties is used for designing the neat and clean webpages to view in different sizes of the screen.

*It helpful to adjust the layout of the webpages as per the different screen sizes. And to avoid the overflow of the content.*

### &#9780; Overview:
1. [Media queries](#-media-queries)
2. [Flexible layouts](#-flexible-layouts)
3. [Responsive images](#-responsive-images)
4. [Fluid typography](#-fluid-typography)
5. [Flexbox or Grid](#-flexbox-or-grid)
6. [Important Key Points](#-important-key-points)

### &#10022; Media queries:
The conditional statements that allow to apply styles based on the screen size or other device characteristics

*Syntax:*
```css 
@media screen and (min-width: 768px) {
  /* Styles for screens wider than 768 pixels */
}
```

*Example:*
```css
@media screen and (max-width: 600px) {
  h1 {
    font-size: 24px;
  }
}
```

### &#10022; Flexible layouts:
The layouts that adapt to different screen sizes by using [relative units](./css-units.md) and flexible properties.

```css
div {
  max-width: 100%;
  height: auto;
}
```

### &#10022; Responsive images:
This will automatically adjust the size of the images to fit the screen by applying [relative units](./css-units.md) or using [source tags](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/source-tag.md).

```xml
<img src="image.jpg" alt="Image" width="100%">
```

```xml
<picture>
  <source media="(min-width: 768px)" srcset="image-large.jpg">
  <source media="(min-width: 480px)" srcset="image-medium.jpg">
  <img src="image-small.jpg" alt="Image">
</picture>
```

### &#10022; Fluid typography:
This will adjusts the text font size based on the screen width.

```css
body {
  font-size: calc(16px + (20 - 16) * ((100vw - 320px) / (1280 - 320)));
}
```
```css
@media screen and (max-width: 768px) {
  body {
    font-size: 18px;
  }
}
```

### &#10022; Flexbox or Grid:
| Flexbox | Grid |
| --- | --- |
| Flexbox has meaning in the name itself as Flexible boxes. Which does not need to follow the parent or other sibling elements. It need to be flexible with the parent element sizes. | Grid has meaning in the name itself as valid a grid connections. That means each items will be interconnected and follows and transfers the properties of grid to each elements. |
| Flexbox will gives flexible arrangements. | Grid will gives rigid layout. | 
| Flexbox is used for the elements are to be fine with uneven sizing. | Grid is used for the elements need to be even and perfect in sizing. |
| Flexbox will flexes the items into the single row immediately as defined.| Grid will not arrange then into the single row.|
| `flex-direction: row;` is the default value takes place to arrange in the single row. | `grid-auto-flow: row;` is the default value takes place to not arrange them in the single row. |
| `flex-wrap: wrap;` gives the improper wrapping behavior. | Here, Wrapping behavior defined by creating grid layout `grid-template-columns: value;` |
| Flexbox is also creating and dealing with 2 dimensional layout. | Grid is also creating and dealing with 2 dimensional layout. |
| Flexbox has each row is independent to the next and each other. | Grid strictly follow the arrangement of grid items with previous rows and columns. |
| Flexbox can be wrapped over different screen sizes to fit in the box. | Grid needs to define the layout for each screen size ranges as become a neat layout. |
| Flexbox does have only limited control over the structure from parent perspective. | Grid gives the control over the structure from parent perspective. |
| Flexbox gives intrinsic sizing of flex items. That each flex items will take required space and gap to make more flexible in the main axis or direction. | Grid allocates the same sizing and spacing for all grid items until if different layouts are defined and applied. |
| Flexbox is preferred to be used on lots of elements and small layouts. | Grid is preferred to be used on large scale layouts. |
| Flexbox is suitable for if need to be considered more on wrapping the elements. | Grid is suitable for if need to be follow more on layout basis. |


### &#10022; Important Key Points:
- To avoid overflow of parent and child elements, use the `max-width` property. This means the element will gets expanded until that maximum width. When it meets the smaller screen sizes than described maximum width, Then it will shrinks and wraps to what is minimum of the size as possible.
- To avoid over shrink or wrapping of element, use the `min-width` property. 
- The vertical overflow or shrink of element, use `min-height` and `max-height` property.
- For images, Set `max-width` property to `100%`, That will not allow images to overflow by its actual sizes.
- Avoid Fixed Size Units in CSS like pixel. Use relative units like Percentage, Em, Rem, Vw, Vh and so on.
- Use `min`, `max` and `clamp` functions to deal with responsive units to the property of the elements.
- Use `@media` queries for different screen sizes and devices. When comes to avoid complexity of the CSS, do not write the all other properties are replaced by `@media` queries. see the below example.

```css
/* Adding flex to the parent in complex */
.parent-element {
  display: flex;
  gap: 1em;
  border-radius: 12px;
}

@media(max-width: 500px) {
  .parent-element {
    display: block;
  }
}

/* 
  These above flex items style re-written as simpler.
  By default, The .parent-element has display property as block.
  This is called mobile first responsive design pattern with minimal amount lines.
*/
.parent-element {
  border-radius: 12px;
}

@media(min-width: 500px) {
  .parent-element {
    display: flex;
  }
}
```

---
[&#8682; To Top](#-responsive-design)

[&#10094; Previous Topic](../docs/borders-and-outlines.md) &emsp; [Next Topic &#10095;](../docs/css-animations.md)

[&#8962; Goto Home Page](../README.md)
