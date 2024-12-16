## &#9873; Layouts
These properties is used for arrangement of elements to create different layouts to the HTML document.

*There are 3 popular layout properties in CSS. That are display, position and float.*

### &#9780; Overview:
1. [Block-level elements](#-block-level-elements)
2. [Inline elements](#-inline-elements)
3. [Inline-block elements](#-inline-block-elements)
4. [Flexbox layout](#-flexbox-layout)
5. [Grid layout](#-grid-layout)
6. [Positioning](#-positioning)
7. [Floating elements](#-floating-elements)

### &#10022; Block-Level Elements:
This type of elements take up the full width of their container and create a new line after them.

*Example: `<div>, <p>, <h1>-<h6>, <ul>, <ol>, <form>, <table>`*

### &#10022; Inline Elements:
This type of elements that do not start on a new line and only take up the space they need.

*Examples: `<span>`, `<a>`, `<em>`, `<strong>`, `<img>`, `<input>`, `<button>`*

### &#10022; Inline-Block Elements:
The elements that has combination of the characteristics of block-level and inline elements.

*Syntax: `display: inline-block;`*

```css
.my-element {
  display: inline-block;
}
```

### &#10022; Flexbox Layout:
This is a flexible layout system for arranging items in a container.

*Syntax: `display: flex;`*

```css
.container {
  display: flex;
  /* required flexbox properties */
}
```

To know more about [`flexbox`](./css-flexbox.md)

### &#10022; Grid Layout:
This is a grid-based layout system for creating complex layouts.

*Syntax: `display: grid;`*

```css
.container {
  display: grid;
  /* required grid properties */
}
```

To know more about [`grid`](./css-grid.md)

### &#10022; Positioning:
It determines the element that where should be placed on the parent or the page. There are 5 common positioning type in CSS. That are Static, Relative, Absolute, Fixed, Sticky.

- Static Position:
  - This is a default positioning in the elements. Which are positioned according to their normal flow.
  - *Syntax: `position: static;`*
  
  ```css
  div {
    position: static;
  }
  ```

- Relative Position:
  - The elements are positioned relative to their normal position
  - *Syntax: `position: relative;`*
  
  ```css
  div {
    position: relative;
  }
  ```

- Absolute Position:
  - The elements are positioned relative to their nearest positioned ancestor or the initial containing block.
  - When assign the position to absolute for any of the child element inside container. Which will be positioned to the document body when parent element does not assigned to relative positioning.
  - *Syntax: `position: absolute;`*
  
  ```css
  div {
    position: absolute;
  }
  ```

- Fixed Position:
  - The elements are positioned relative to the viewport.
  - *Syntax: `position: fixed;`*
  
  ```css
  div {
    position: fixed;
  }
  ```

- Sticky Position:
  - This is a hybrid of relative and fixed positioning. This elements are initially positioned relative to its parent element. As the element scrolls past its parent's top edge, it becomes fixed relative to the viewport until it reaches its bottom edge.
  - *Syntax: `position: static;`*
  
  ```css
  div {
    position: static;
  }
  ```

### &#10022; Floating Elements:
The elements are removed from the normal flow and placed to the left or right.

*Syntax: `float: left;` or `float: right;`*

```css
img {
  float: left;
}
```

---
[&#8682; To Top](#-layouts)

[&#10094; Previous Topic](../docs/color-and-background.md) &emsp; [Next Topic &#10095;](../docs/borders-and-outlines.md)

[&#8962; Goto Home Page](../README.md)
