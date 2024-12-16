## &#9873; CSS Flexbox:
These properties are used to give and control the flexibility over the element and the layout.

*The elements are treated as flex item. By assigning the property, `display: flex;` to the parent element.*

### &#9780; Overview:
1. [Setting Flex Items](#-setting-flex-items)
2. [Flex Shrink](#-flex-shrink)
3. [Gap Property](#-gap-property)
4. [Flex Grow](#-flex-grow)
5. [Flex Wrap](#-flex-wrap)
6. [Flex Basis](#-flex-basis)
7. [Flex Direction](#-flex-direction)
8. [Justify Content](#-justify-content)
9. [Align Items](#-align-items)
10. [Align Self](#-align-self)
11. [Note](#-note)

### &#10022; Setting Flex Items:
It will defines the flex items for their children elements.

*Syntax: `display: flex;`*

```css
.parent-element {
  display: flex;
}
```
> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		/* Additional Styling */
		list-style: none;
		margin: 0;
		padding: 0;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Flex Shrink:
Flex Shrink property is used to avoid overflow of flex items from the parent box container or to wrap the flex items, when the parent does not has the enough space for the flex items to fit in it. Due to different device screen size.

*Default flex shrink value is 1. So, That If flex items does not have enough space inside the parent container, Then first, it wraps the content inside the flex items. Finally, wrap the flex items into new line. If it is set to 0, Then the flex items will not be shrink and overflow out of the parent container element.*

*Syntax: `flex-shrink: 1;`*

```css
.parent-element {
  display: flex;
}

.flex-items {
	flex-shrink: 1;
}
```
> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
	}

	nav li {
		flex-shrink: 1;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Gap Property:
This property is used to add some space between flex items on both co-ordinates.

*Syntax: `gap: value;`*

```css
.parent-element {
  display: flex;
  gap: 1em;
}
```
> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		gap: 1em;
	}

	nav li {
		flex-shrink: 1;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Flex Grow:
Flex Grow property is used to grow the flex items when the parent has the enough space. That space is evenly distributed to all flex items.

*Default flex grow value is 0. If it is set to 1, Then the flex items will be grow to fill the available space in the parent element.*

*Syntax: `flex-grow: 0;`*

```css
.parent-element {
  display: flex;
}

.flex-items {
	flex-grow: 0;
}
```
> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		gap: 1em;
	}

	nav li {
		flex-shrink: 1;
		flex-grow: 0;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Flex Wrap:
Flex wrap property is used to wrap the flex items when there is no enough space for flex items inside parent container.

*Default flex wrap value is `nowrap`. If it is set to wrap, Then the flex items will be wrap into new line inside the parent container element.*

*Syntax: `flex-warp: wrap;`*

```css
.parent-element {
  display: flex;
  flex-wrap: wrap;
}
```
> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		gap: 1em;
		flex-wrap: wrap;
	}

	nav li {
		flex-shrink: 1;
		flex-grow: 0;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Flex Basis:
Flex basis property is used to control the flex items size and how much size should take each.

*Default flex basis value is `auto`. If it is set to 0, Then all of the flex items sizes will be set to same based on the [`flex-grow`](#-flex-grow) property and [`flex-shrink`](#-flex-shrink) property values assigned to it.*

*On the other hand, These three above properties can be re-written in the short form as `flex: value;`. Which mentions that `flex-grow: 1;` `flex-shrink: 1;` `flex-basis: 0;`.*

*Syntax: `flex-basis: 0;`*

```css
.parent-element {
  display: flex;
  flex-basis: 0;
}
```

*There is slight difference between `width: value;` property and `flex-basis: value;`. That is, the width property will forced to set width of the element. For example, take `width: 0px` and `flex-basis: 0px`. Flex basis will not set size to 0 pixels. But it maintain some reasonable width as not as width property.*

*When using flex basis property, Then [`flex-shrink`](#-flex-shrink) and [`flex-grow`](#-flex-grow) property to be assigned to grow or shrink. If these two properties is not given then the default value taken into action. Thats normal. But if these two properties is set to 0, Then the flex-basis will act as width property of the flex items. Thus the flex items will not allowed to fit in the parent container element. Either that will be shorter or Overflowed out of the parent container element.*

> Setting same size of 300px to all flex items.
```css
.parent-element {
	display: flex;
	flex-basis: 300px;
}
```

> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		gap: 1em;
		flex-wrap: wrap;
		flex: 0;
	}

</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Flex Direction:
The flex direction property will defines the arrangements of flex items. Either to be arranged in row axis or to be stacked in one by one in the column axis.

*The default flex direction value is `row`. So, The flex direction defines which axis is the main axis for the flex items.*

*Syntax: `flex-direction: value;`*
> The flex items arranged horizontally.
```css
.parent-element {
  display: flex;
  flex-direction: row;
}
```
> The flex items arranged vertically.
```css
.parent-element {
  display: flex;
  flex-direction: column;
}
```

> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		flex-direction: row;
		/* Additional Styling */
		list-style: none;
		margin: 0;
		padding: 0;		
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Justify Content:
Justify content property is used to arrange the flex items in the main direction. Which is mentioned by the `flex-direction` property. 

*When deals with justify content property, Avoid [`flex-grow`](#-flex-grow) property. Because, all left over space will be taken to grow the flex items and there is no more spaces for justifying the flex items. That is meaningless and useless.*

**List of Justify Content Values:**
- `flex-start` - It is default value. It will arrange to the starting point of the main direction.
- `flex-end` - It will arrange to the ending point of the main direction.
- `center` - It will arrange to the center of the main direction.
- `space-between` - It will add same spaces between each flex items by using left over spaces in the main direction. 
- `space-around` - It will add same spaces around the each flex items to main direction from left over spaces in the main direction. 
- `space-evenly` - It will add even spaces on both sides of each flex items to main direction from left over spaces in the main direction. 

*Syntax: `justify-content: value;`*
> The flex items arranged in center to main direction.
```css
.parent-element {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
```

> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		/* Additional Styling */
		list-style: none;
		margin: 0;
		padding: 0;		
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Align Items:
Align Items property is used to align the flex items in the cross axis or direction to the main direction. The main axis or direction is defined by the `flex-direction` property. 

*When it is said to be main axis or direction, Then that axis or direction has more flex items on it. As counted on the basis of the axis or direction.*

**List of Justify Content Values:**
- `stretch` - It is default value. It will stretch the height of the smaller flex items to the maximum content fit size of the parent container element.
- `flex-start` - It will align to the starting point of the cross axis or direction.
- `flex-end` - It will align to the ending point of the cross axis or direction.
- `center` - It will aligns to the center of the cross axis or direction.

*Syntax: `align-items: value;`*
> The flex items aligned in center to cross axis or direction.
```css
.parent-element {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
```

> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		/* Additional Styling */
		list-style: none;
		margin: 0;
		padding: 0;		
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Align Self:
Align Self property is used to align the specific flex item in the cross axis or direction to the main direction. Which is similar to the [`Align Items`](#-align-items) property. But it will avoid parent flex alignment.

**List of Justify Content Values:**
- `stretch` - It is default value. It will stretch the height of the smaller flex item to the maximum content fit size of the parent container element.
- `flex-start` - It will align to the starting point of the cross axis or direction.
- `flex-end` - It will align to the ending point of the cross axis or direction.
- `center` - It will aligns to the center of the cross axis or direction.

*Syntax: `align-self: value;`*
> The flex item aligned in start to cross axis or direction.
```css
.parent-element {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.children {
	align-self: flex-start;
}
```

> Demonstrating with navigation element
```xml

<style type="text/css">
	nav {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		/* Additional Styling */
		list-style: none;
		margin: 0;
		padding: 0;		
	}

	nav li:active {
		align-self: flex-start;
	}
</style>

<nav>
	<li><a href="#home">Home</a></li>
	<li><a href="#about">About</a></li>
	<li><a href="#service">Service</a></li>
	<li><a href="#contact">Contact</a></li>
</nav>

```

### &#10022; Note:
- There is no `justify-self` for flex items. And also it does not make any sense. The `justify-self` property is useful for [`CSS Grid`](./css-grid.md).
- To make the flex items to be same as the sibling rows like grid then use these properties.
```css
/* 
	To arrange flex items such as 3 items in row to be filled in the remaining space.
	And if any left over element at the last that grow to entire width of the parent container.
	This will looks like grid but it is a flexible boxes.
*/
flex-grow: 1;
flex-basis: 33.33%
```

---
[&#8682; To Top](#-css-flexbox)

[&#10094; Goto Layouts Topic](./layouts.md)

[&#8962; Goto Home Page](../README.md)