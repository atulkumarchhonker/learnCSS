## &#9873; CSS Selectors
The CSS Selectors are used to target specific elements in an HTML document to assign value for their property to apply styles to them.

*There are almost 9 type of selectors in CSS.*

### &#9780; Overview:
1. [Element Selectors](#-element-selectors)
2. [Class Selectors](#-class-selectors)
3. [ID Selectors](#-id-selectors)
4. [Universal Selector](#-universal-selector)
5. [Descendant Selectors](#-descendant-selectors)
6. [Child Selectors](#-child-selectors)
7. [Adjacent Sibling Selectors](#-adjacent-sibling-selectors)
8. [General Sibling Selectors](#-general-sibling-selectors)
9. [Attribute Selectors](#-attribute-selectors)

### &#10022; Element Selectors:
It targets the elements based on their tag name.

*Syntax: `tag_name`*

```css
p {
  color: blue;
}
```

### &#10022; Class Selectors:
It targets elements based on a class attribute.

*Syntax: `.class_name`*

```xml
<div class="my-class">This is a div with some content</div>
```

```css
.my-class {
  font-weight: bold;
}
```

### &#10022; ID Selectors:

It targets a single element based on its unique ID attribute.

*Syntax: `#id_name`*

```xml
<h1 id="my-heading">This is a heading</h1>
```

```css
#my-heading {
  text-align: center;
}
```

### &#10022; Universal Selector:

It targets all elements in the HTML document.

*Syntax: `*`*

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### &#10022; Descendant Selectors:
It targets elements that are descendants of another element.

*Syntax: `parent_element child_element`*

```css
div p {
  color: green;
}
```

### &#10022; Child Selectors:
It targets elements that are direct children of another element.

*Syntax: `parent_element > child_element`*

```css
div > p {
  color: green;
}
```

### &#10022; Adjacent Sibling Selectors:
It targets the next element that is a sibling of the current element.

*Syntax: `element1 + element2`*

```css
p + span {
  font-style: italic;
}
```

### &#10022; General Sibling Selectors:
It targets all elements that are siblings of the current element.

*Syntax: `element1 ~ element2`*

```css
h1 ~ p {
  color: red;
}
```

### &#10022; Attribute Selectors:
It targets elements based on their attributes.

*Syntax:* 
- `[attribute_name]`
- `[attribute_name="value"]`
- `[attribute_name^="value"] (starts with)`
- `[attribute_name$="value"] (ends with)`
- `[attribute_name*="value"] (contains)`

> Apply style to the a tag having the attribute name
```css
a[href] {
  color: blue;
}
```

> Apply style to the a tag with attribute value equals to `aboutus.html` 
```css
a[href="aboutus.html"] {
  color: blue;
}
```

> Apply style to the a tag with attribute value starts with `https://` 
```css
a[href^="https://"] {
  color: blue;
}
```

> Apply style to the a tag with attribute value ends with `.html` 
```css
a[href$=".html"] {
  color: blue;
}
```

> Apply style to the a tag with attribute value contains `products` 
```css
a[href*="products"] {
  color: blue;
}
```
---
[&#8682; To Top](#-css-selectors)

[&#10094; Previous Topic](../introduction.md) &emsp; [Next Topic &#10095;](./pseudo-selectors.md)

[&#8962; Goto Home Page](../README.md)
