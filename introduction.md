## &#9873; Introduction to CSS

### &#10022; What is CSS?
CSS is stands for `Cascading Style Sheet`. CSS is used to style the HTML elements and Web Pages, To make rich and nice layout for easy access.

### &#10022; How CSS Works with HTML?
CSS will apply styles to the HTML elements as a top to bottom approach. Which means the CSS style will be applied into web pages as line by line based on selectors and it's properties and values.

CSS styles are mainly used for presenting and styling the web pages as per the requirements. Without CSS Styles, the web pages, you have seen now will be a skeleton alone.

> HTML document
```xml
<!DOCTYPE html>
<html>
<head>
	<title>Page Title</title>
	<link rel="stylesheet" type="text/css" href="main.css" media="all" />
</head>
<body>

	<h1>Heading 1</h1>
	
	<p>This is a paragraph</p>

</body>
</html>
```

> main.css file
```css
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
```

### &#10022; Basic Syntax and Structure?

- These `{` &nbsp; `}` curly brackets are used to holds bunch of properties for selectors. 
- Where, the asterisk `*` symbol denotes the selector for all visible elements in the HTML document. 
- The `margin:`, `padding:` and `box-sizing:` are properties for elements which is assigned by `:` and followed by value.
- These each properties-value will be ending with symbol `;` semi-colon.

---
[&#8682; To Top](#-introduction-to-css)

[&#10094; Previous Topic](./usage.md)&emsp;[Next Topic &#10095;](./docs/selectors.md)

[&#8962; Goto Home Page](./README.md)