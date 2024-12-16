## &#9873; CSS Units
The CSS Units are used to specify the unit of measurements for value of the properties.

*There are almost 5 type of Units in CSS.*

### &#9780; Overview:
1. [Pixels (px)](#-pixels)
2. [Percentages (%)](#-percentages)
3. [Ems (em)](#-ems)
4. [Rems (rem)](#-rems)
5. [Viewport units (vw, vh, vmax, vmin)](#-viewport-units)
6. [Functions](#-functions)
	- [Min Function](#-min-function)
	- [Max Function](#-max-function)
	- [Minmax Function](#-minmax-function)
	- [Calc Function](#-calc-function)
	- [Clamp Function](#-clamp-function)
	- [Repeat Function](#-repeat-function)

### &#10022; Pixels:
It is a fixed unit of measurement that represents one pixel on the screen.

*Syntax: `value px`*

```css
p {
  font-size: 16px;
}
```

### &#10022; Percentages:
It is a relative unit of measurement that represents a percentage of the parent element's size.

*Syntax: `value %`*

```css
div {
  width: 50%;
}
```

### &#10022; Ems:
It is a relative unit of measurement that represents the font size of the element's parent

*Syntax: `value em`*

```css
p {
  font-size: 1.2em;
}
```

### &#10022; Rems:
It is a relative unit of measurement that represents the font size of the root element (usually the `<html>` element).

*Syntax: `value rem`*

```css
p {
  font-size: 1.5rem;
}
```

### &#10022; Viewport Units:
It is a relative units of measurement based on the viewport size (the visible area of the browser window)

*Syntax:*
- `vw`: Viewport width,
- `vh`: Viewport height,
- `vmax`: Maximum of viewport width and height,
- `vmin`: Minimum of viewport width and height.

```css
div {
  font-size: 2vw;
  height: 100vh;
}
```

### &#10022; Functions:
CSS has predefined functions that may accepts certain parameters. Which return value for the properties to assign them.

**The list of commonly used functions:**
- [`min()`](#-min-function)
- [`max()`](#-max-function)
- [`minmax()`](#-minmax-function)
- [`clamp()`](#-clamp-function)
- [`repeat()`](#-repeat-function)

### &#10022; Min Function:
It will give the minimum value among the comma separated given units by comparing them. 

*This will gives smallest (most negative) value from the list of comma separated values.*

*This function can be used anywhere that accepts the units such as `number`, `integer`, `percentage`, `length`, `angle`, `time`, `frequency`.*

*Syntax: `min(value1, value2);`*

> The example assigns the minimum possible width either 800px or 90%. 
```css
.container {
	width: min(800px, 90%);
}
```

> The long description of the above min function can be possible by the below code.
```css
.container {
	width: 800px;
	max-width: 90%;
}
```

*This `min` function will set width to the container that if 800px is smaller than 90% of the viewport then it will return 800px as value and vice versa.*

### &#10022; Max Function:
It will give the maximum value among the comma separated given units by comparing them. 

*This will gives largest (most positive) value from the list of comma separated values.*

*This function can be used anywhere that accepts the units such as `number`, `integer`, `percentage`, `length`, `angle`, `time`, `frequency`.*

*Syntax: `max(value1, value2);`*

> The example assigns the maximum possible width either 200px or 90%. 
```css
.container {
	width: max(200px, 90%);
}
```

> The long description of the above max function can be possible by the below code.
```css
.container {
	width: 90%;
	min-width: 200px;
}
```

*This `max` function will set width to the container that if 200px is larger than 90% of the viewport then it will return 200px as value and vice versa.*

### &#10022; Minmax Function:
This function in CSS is used to specify a range of values for a property, allowing you to set a minimum and maximum value for a property. This is particularly useful for creating responsive layouts and ensuring that elements don't become too large or too small.

*Syntax: `minmax(min-value, max-value)`*
 
```css
.container {
	width: minmax(300px, 80%);
}
```

### &#10022; Calc Function:
This function in CSS is used to performs mathematical calculations on CSS values.

*Syntax: `calc(expression)`*
 
```css
.container {
	width: calc(100% - 20px);
	margin: calc(2rem / 2);
}
```

### &#10022; Clamp Function:
This function in CSS is used to clamps a value between a minimum and maximum.

*Syntax: `clamp(min-value, preferred-value, max-value)`*
 
```css
.container {
	font-size: clamp(12px, 2vw, 24px);
}
```

### &#10022; Repeat Function:
This function in CSS is used to repeat a value to the specified number of times.

*Syntax: `repeat(count, value)`*
 
```css
.container {
	grid-template-area: repeat(3, 1fr);
}
```

---
[&#8682; To Top](#-css-units)

[&#10094; Previous Topic](../docs/properties-and-values.md) &emsp; [Next Topic &#10095;](../docs/text-styling.md)

[&#8962; Goto Home Page](../README.md)
