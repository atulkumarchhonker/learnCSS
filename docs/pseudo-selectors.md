## &#9873; Pseudo Selectors
It allows to style elements based on their state or relationship to other elements. They provide additional flexibility in CSS styling.

*There are 3 common type of pseudo-selectors in CSS.*

### &#9780; Overview:
1. [Structural Pseudo Selectors](#-structural-pseudo-selectors)
2. [State Pseudo Selectors](#-state-pseudo-selectors)
3. [Content Pseudo Selectors](#-content-pseudo-selectors)

### &#10022; Structural Pseudo Selectors:
This type of pseudo-selectors targets element based on the HTML document positions. 

*The list of structural pseudo-selectors:*
  - :root: Targets the root element of the document (typically <html>).
  - :first-child: Targets the first child element of its parent.
  - :last-child: Targets the last child element of its parent.
  - :nth-child(n): Targets the nth child element of its parent, where n is an integer.
  - :nth-of-type(n): Targets the nth element of a specific type within its parent.
  - :only-child: Targets an element that is the only child of its parent.
  - :first-of-type: Targets the first element of a specific type within its parent.
  - :last-of-type: Targets the last element of a specific type within its parent.
  - :only-of-type: Targets an element that is the only element of its type within its parent.
  - :empty: Targets an element that has no children.
  - :target: Targets an element that is the current target of a hyperlink.
  - :not(): Targets elements that do not match a specified selector or set of selectors.
  - :has(): Targets elements that have a specific child or descendant element or property or value or anything related to the element.

```css
/* Root pseudo-selectors used for defining CSS variables */
:root {
  --text-color: black;
}

/* This will set style to first child of the div elements */
div:first-child {
  color: blue;
}

/* not pseudo-selectors */
button:not(:first-child) {
  ...
}

/* has pseudo-selectors */
button:has(.icon-button) {
  ...
}

button:has(svg) {
  ...
}

/* light and dark theme selection based css selector */
body:has(#theme option[value="dark"]:checked) {
  background: black;
  color: white;
}
```

### &#10022; State Pseudo Selectors:
It targets elements based on their current state of behavior.

*The list of structural pseudo-selectors:*
  - :hover: Targets an element when the mouse pointer is hovering over it.
  - :active: Targets an element when it is activated (e.g., clicked or tapped).
  - :focus: Targets an element when it is focused (e.g., by keyboard or mouse).
  - :visited: Targets an element that has been visited by the user.
  - :link: Targets an anchor element that has not been visited.
  - :checked: Targets a checked input element (e.g., checkbox, radio button).
  - :disabled: Targets a disabled element.
  - :enabled: Targets an enabled element.
  - :focus-within: Targets an element and its descendants when any of them is focused.

```css
/* It bolds the text of anchor tag when it is hovered */
a:hover {
  font-weight: bold;
}
```

### &#10022; Content Pseudo Selectors:
It targets a element on before or after basis.

```css
/* This will insert '+' before the paragraph tag */
p::before {
  content: "+";
  color: red;
}

/* This will insert '\' after the paragraph tag */
p::after {
  content: "\";
  color: blue;
}
```

---
[&#8682; To Top](#-pseudo-selectors)

[&#10094; Previous Topic](./selectors.md) &emsp; [Next Topic &#10095;](./properties-and-values.md)

[&#8962; Goto Home Page](../README.md)
